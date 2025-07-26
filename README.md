# nvim-config
My file I use for neovim.

# What does it have?
- A C++ language server (autocompleting), syntax highlighting
- A file explorer (or called a tree in programming) by running :NvimTreeOpen
- C++ code running within neovim by pressing \ and then r (and it will wait until execution or you can exit by press CRTL + C)
- Commenting by press g and then c

# Setup (linux)
1. Install neovim
2. ```cd ~/.config/nvim``` then ```sudo nano init.vim```
3. Paste in the config file
4. Replace this line ```nnoremap <leader>r :w<CR>:!g++ % -o %< && ./%< && read -p "Press any key to continue..."<CR>``` with ```nnoremap <leader>r :w<CR>:!bash -c 'g++ % -o %< && ./%<; read -n 1 -s -r -p "Press any key..."'<CR>```
5. Run ```nvim``` and press ```:``` and then type ```PlugInstall```
6. Then, restart neovim and you should be good to go
