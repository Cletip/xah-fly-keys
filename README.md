



Tout ce que j'ai à faire pour le conserver à jour : 



sur master (normalement c'est bon, faire un git status)
git pull --rebase upstream master
git push --force-with-lease origin master




ancien : 

https://reflectoring.io/github-fork-and-pull/#Updating-your-Fork

magit :

1. fetch upstream
2. me mettre sur master (normalement c'est déjà bon)
3. faire un merge avec upstream/master

si cela na marche pas : 

1. git remote add upstream https://github.com/xahlee/xah-fly-keys
2. git fetch upstream
3. dans magit, faire un merge (m m)avec upstream/master, et normalement push (si je suis bien sous origin/master)

# Le readme

Dans ce readme, je suppose que vous utiliser straight ou use-package (ou les deux) correctement.

## Speed Installation


Pas sûr de ceci :

```elisp
(use-package xah-fly-keys
   ;; :after (xah-fly-keys)
    :straight '(xah-fly-keys :host github
			:repo "Cletip/xah-fly-keys"
			:branch "main"
			:files ("*.el" "out")
			)
    
    )
```


##  Comment 

Ceci est une "surcouche" de Xah fly keys qui permet de simplifier certaines utilisations. Elle nécessite d'autres packages (si une commande ne marche pas, regarder le nom de la commande et télécharger le package sur internet).

Le but de ce package et d'ajouter des raccourcis au package xah-fly-keys. De
plus, "SPC ENT"  permet d'appeler un menu différent à chaque major mode. Ce n'est pas vraiment dans la philosophie de xah-fly-keys, mais je trouve ça très pratique dans certains cas.


You can install xah-fly-keys like this (minimal configuration):  
  
```elisp
(use-package xah-fly-keys	     
    :config
     ;;chose your layout
    (xah-fly-keys-set-layout "azerty")

    (xah-fly-keys) ;;activate xah fly keys

    )
```  






xah-fly-keys
===================

A modal keybinding for emacs (like vim), but based on command frequency and ergonomics.

This is the most efficient editing system in the universe.

Xah Fly Keys home page at
http://xahlee.info/emacs/misc/xah-fly-keys.html

2020-04-18 News: Key Engine Rewrite
===================

Major key engine rewrite by Dan Langlois (https://github.com/DanLanglois) and Will Dey (https://github.com/wi11dey) .

QWERTY layout
-------------------
![xah-fly-keys qwerty layout](xah_fly_keys_qwerty_layout_2020-04-18_4fgyk.png)

Manual Install
-------------------

put the file xah-fly-keys.el in ~/.emacs.d/lisp/
create the dir if doesn't exist.

put the following in your emacs init file:

```elisp

(add-to-list 'load-path "~/.emacs.d/lisp/")

(require 'xah-fly-keys)

;; specify a layout
(xah-fly-keys-set-layout "qwerty")

;; possible values
;; adnw , azerty , azerty-be , beopy , bepo , carpalx-qfmlwy , carpalx-qgmlwb , carpalx-qgmlwy , colemak , colemak-dhm , colemak-dhm-angle , colemak-dhk , dvorak , koy , neo2 , norman , programer-dvorak , pt-nativo , qwerty , qwerty-abnt , qwerty-no (qwerty Norwegian) , qwertz , workman

(xah-fly-keys 1)
```

Full Documentation
-------------------

http://xahlee.info/emacs/misc/xah-fly-keys.html

Been working on this since 2013, and since 2007 on ergoemacs-mode.

give me 5 bucks https://paypal.com pay to Xah@XahLee.org

Thanks.
