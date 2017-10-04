








** Installer l'extension "Chrome Extension Source code Viewer"
https://chrome.google.com/webstore/detail/chrome-extension-source-v/jifpbeccnghkjeaalbbjmodiffmgedin/related


** REFERENCES

Pour accéder au dossier où sont rangées les extensions chrome :
https://www.parlonsgeek.com/visualiser-code-source-dune-extension-chrome/

Images fabriquées à partir de :
https://www.flaticon.com/free-icon/nut-icon_69398


** AJOUTER UNE ENTREE DE MENU CONTEXTUEL CHROME

Pour ajouter une entrée dans le menu contextuel sur Chrome, il suffit d'ajouter, à la fin du fichier background.js :

chrome.contextMenus.create({
    "title": chrome.i18n.getMessage("addToTodoist"),
    "contexts": ["page", "selection", "link"],
    "onclick": addToTodoistFromMenu
});

EXPLICATION DE CE CODE

- Le message affiché "addToTodoist" provient des messages situées dans _locales/xx/messages.json
- L'action lancée est "addToTodoistFromMenu" et elle est située dans background.js, un peu plus haut :

/*
 * Context menu adding
 */
function addToTodoistFromMenu(ev, tab) {
...
}

