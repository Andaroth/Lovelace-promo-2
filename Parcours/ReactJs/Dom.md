# React

## Table des matières

- [installation](./Installation.md)   
- [Introduction](./introduction.md)
- [Dom](./Dom.md) ←


## Introduction
Alors, on n'a vu comment créer un component et en créer un deuxième les uns dans les autres mais on ne sais toujours pas comment et pourquoi les afficher.

React utilise un principe utilisant le "virtual dom". En fait, il va simplement créer une page virtuellement puis seulement l'afficher quand on lui demande.

Ici, dans index.js on import le component App et il y a un ReactDOM.render(<App />, document.getElementById('root'));

Pour faire simple, il créé notre vue et l'affiche à l'emplacement de l'ID root qui se trouve dans index.html


![Giphy](https://www.acsu.buffalo.edu/~cas7/gifs/react.gif)


Rendez-vous à la prochaine leçon: [props](./props.md).


