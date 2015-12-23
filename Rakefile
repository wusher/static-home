task :update do 
  port = ENV['PORT'] || '3000'
  if system("curl -o index.html http://blog.wusher.net/about/me")
    file = File.read 'index.html'
    file.gsub!(/(href|src)="\//, '\1="http://blog.wusher.net/')
    File.open('index.html', 'w') { |f| f.write file }


  else
    puts "Failed to download site"
  end
end
