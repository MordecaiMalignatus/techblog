# frozen_string_literal: true

require 'date'

task default: :new

desc 'Run the Jekyll server locally with rendered drafts.'
task :serve do
  sh 'bundle exec jekyll serve --drafts'
end

desc 'Publishing a draft'
task :publish do
  current_drafts = Dir.glob('./_drafts/*.md')
  puts 'Which entry to publish?'
  current_drafts.each_with_index do |draft, index|
    puts "#{index} -- #{draft}"
  end
  input = $stdin.gets.chomp.strip.to_i

  puts "publishing #{current_drafts[input]}..."
  file_name = current_drafts[input].split('/')[-1]
  current_date = DateTime.now.to_date.to_s
  draft_body = File.read(current_drafts[input])

  new_file = "./_posts/#{current_date}-#{file_name}"
  File.write(new_file, draft_body)
  File.delete(current_drafts[input])

  build_site
  push "Post: #{current_drafts[input]}"
end

desc 'Rerender the site, because the layout or other assets have changed.'
task :rerender do
  build_site
  push 'Chore: Rerender'
end

desc 'Generating a new draft'
task :new do
  print 'title: '
  title = $stdin.gets.chomp.strip
  cleaned_title = title.downcase.gsub(/[[:punct:]]/, '').gsub(/\s/, '-')
  formatted_title = "./_drafts/#{cleaned_title}.md"

  File.write(formatted_title, mkheader(title))
end

def mkheader(title)
  <<~DOC
    ---
    layout: post
    author: Mordecai
    title: "#{title}"
    ---

  DOC
end

def build_site
  sh 'bundle exec jekyll build -d ./docs'
end

def push(commit_msg)
  sh 'git add docs/'
  sh 'git add _drafts/'
  sh 'git add _posts/'
  sh "git commit -m '#{commit_msg}'"
  sh 'git push'
end
