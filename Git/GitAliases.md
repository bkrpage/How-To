# Helpful git Aliases

```
g config --global alias.d   'checkout'
g config --global alias.da  'checkout -- .'
g config --global alias.c   'commit -m'
g config --global alias.ca  '!git add -A && git commit -m ' 
g config --global alias.a   'add'
g config --global alias.aa  'add .'
g config --global alias.p   '!git push origin $(git rev-parse --abbrev-ref HEAD)'
g config --global alias.fp  'fetch -p'
g config --global alias.f   'fetch'
g config --global alias.ch  'checkout'
g config --global alias.n   'checkout -b'  
g config --global alias.chb 'checkout -b'
g config --global alias.chn 'checkout -b'
```