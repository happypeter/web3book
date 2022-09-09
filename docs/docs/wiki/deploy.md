《 Web3.0 架构》

## Generate new img

- Screenshot a fullscreen Keynote slide
- `convert input.png -resize 50% output.jpg`

## Deploy new version

- Edit Text, Add jpg to /imgs
- run `gitbook serve` imgs folder will be copied to /_book/imgs
- `mv _book docs`
- push, and I am ready to go.

## Office word format
- wirte episode title buy hand, from summary.md use h1 as format
- 11pt for text main
- copy text from md file
- change the title for each part as h2
- a blank line after each paragraph/chapterTitle/episodeTitle, no blank line after section title
- run 'git serve' and copy img from localhost:4000 to shimo.im
- everytime I need to modify sth, do the changes in .md file, then copy again
  to shimo
- do shimo to docx backup very often
