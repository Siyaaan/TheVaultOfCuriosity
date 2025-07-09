

:map <F5> :w<CR>:!javac % && java %:r<CR>

Now every time you press F5, it will:

    Save the file

    Compile the current Java file

    Run it using the class name