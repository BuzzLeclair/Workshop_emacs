# **\[Workshop ASTEK\] Emacs configuration**

## **Setup**

1. If you have `.emacs` directory at your root, delete it.
2. Create a `.emacs.d` directory at your root.
3. In the `~/.emacs.d/`, create a `init.el` file and a `configuration.el` file.
4. Make sure emacs is not opened in a graphical window but in a terminal (like during exams, check "no window emacs") 

`init.el` will be the main file that will be loaded when you open emacs. `configuration.el` will contain all the configuration that you will write.

### In elisp (the emacs programming language), when you put (function_name) in brackets, it means that you want to call the function (like you would call **white-space-mode**).

---

## **Packages**

In order to be able to install packages in emacs, you need to set up the archives links.</br>
In the `init.el` file, [Setup](https://www.emacswiki.org/emacs/InstallingPackages) the folowing package archives:
   - org: [http://orgmode.org/elpa/](https://orgmode.org/elpa.html)
   - gnu: http://elpa.gnu.org/packages/
   - melpa-stable: http://stable.melpa.org/packages/
   - melpa: https://melpa.org/packages/

---

## **Lockfiles and backup files**

If you do not know what are lockfiles and backup files, you can read this [documentation](https://www.gnu.org/software/emacs/manual/html_node/emacs/Backup.html). If you don't want them to be created : </br>

In the `init.el` file, make sure that:
   - lockfiles are not created
   - backup files are not created (be careful, as they are sometimes useful if you remove the wrong file !)
---

## **Columns**

We will use the `configuration.el` file to write our configuration, but you can also do it in the init.el, it's just a matter of preference.

If you use the `configuration.el` file, make sure that it is [included](https://www.emacswiki.org/emacs/LoadingLispFiles) in the `init.el` file.


In the file, make sure that the configuration displays the number of columns in your emacs buffer.

---

## **Theme**

**Required package:** dracula-theme

In emacs, install the dracula theme package.

In you configuration file, you need to enable the theme so it is loaded on startup.

---

## **Mouse click**

There's a function in emacs to enable the mouse click in emacs.

In the `configuration.el` file, make sure to call that function and check if each time you open emacs, it's enabled.

---

## **Treemacs**

**Required package:** treemacs

Treemacs is a package that let you navigate through your files and folders in emacs. Like Visual Studio Code.

In emacs :
   - install the treemacs package
   - call the function to enable it in your configuration file.</br></br>

When you open emacs, you should see a new window with a tree of your files and folders. ( Like this !)![image](https://github.com/BuzzLeclair/Workshop_emacs/assets/91875583/59b09dd6-cb09-47f2-9414-78d405d29854)



---

## **Pairs**

**Required package:** electric-pair-mode

In Emacs, there's a function that enables to automatically add a pair of characters when you add one of them.</br>
Install the package and enable it in your configuration file.

Ensure that:
- the `"` character is added to the buffer when you add a `"` character
- the `}` characher is added to the buffer when you add a `{` character
- the `'` character is added to the buffer when you add a `'` character

---

## **Trailing spaces**

In the your configuration file, make sure that trailing spaces are deleted when you save your file by calling a function everytime emacs is open.

---

## **Autocompletetion**

**Required packages:** company, company-c-headers

https://company-mode.github.io/manual/Getting-Started.html


---

## **Shortcuts**

**Required package:** tab-bar-mode

Create a new file called `shortcuts.el`.
You need to call this file in your `init.el`

Ensure that:
   - `Ctrl+n` opens a new tab bar in your emacs buffer
   - `Ctrl+q` closes the tab bar in your emacs buffer
   - `Ctrl+t` opens / closes treemacs
   - `Ctrl+A` adds a new repository to treemacs
   - `Ctrl+D` removes a repository to treemacs

You can add more like copy paste shortcut and more !

---

## **(bonus) - setup lsp-mode**

Look up this emacs documentation on how to run debuginfo (compile your program at runtime to display warnings (inside emacs !))
https://emacs-lsp.github.io/lsp-mode/tutorials/CPP-guide/
