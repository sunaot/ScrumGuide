task :make_html do
  `hikidoc ScrumGuide.hiki > ScrumGuide_ja.html`
  content = ''
  open('ScrumGuide_ja.html', "r+") do |f|
    content = f.read.gsub(/[\r\n]/, '')
  end
  content.gsub!(/<\/head>/, '<link rel="stylesheet" href="./style.css" type="text/css"></head>')
  open('ScrumGuide_ja.html', "w+") do |f|
    f.write(content)
  end
end
