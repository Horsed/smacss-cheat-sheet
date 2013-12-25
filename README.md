cheat sheet for smacss with sass
==================

based on [this article](https://medium.com/objects-in-space/f6f404727) by [Andrew Colclough](https://twitter.com/wtc) (which refers [these other links](#sources))

## pattern

  ```html
  <div class="base-block--specific-block">
    <div class="specific-block__element">
      <div class="element">...</div>
      <div class="element is-active">...</div>
      <div class="element--is-last">...</div>
    </div>
  </div>
  ```

  * blocks define 
  * elements define
  * modifiers define
  * layouts of blocks and elements are defined by their containing blocks

## directory structure
  
  <pre><code>
  css
  ├── <a href="#base">base</a>
  │   ├── fonts.scss
  │   ├── colors.scss
  ├── states
  │   ├── <a href="#statesscss">states.scss</a>
  ├── modules
  │   ├── <a href="#base-blockscss">base-block.scss</a>
  │   ├── <a href="#elementscss">element.scss</a>
  </code></pre>
  
### base

  global styles like fonts, colors

### states.scss

  global **states**

  ```css
  .is-active {
    ...
  }
  ```

### base-block.scss

  ```css
  .base-block { /*style of a block*/
    ...
  }
  
  .specific-block { /*style of a specific block*/
    @extend .parent;
    ...
  }
  
  .specific-block__element { /*layout of an element nested within .specific-block*/
    ...
  }
  ```

### element.scss

  ```css
  .element { /*style of an element*/
    ...
  }
  
  .element--is-last { /*element specific state*/
    ...
  }
  ```

## sources

  * [SMACSS](http://smacss.com/)
  * [BEM](http://bem.info/)
  * [How to Scale and Maintain Legacy CSS with Sass and SMACSS](http://webuild.envato.com/blog/how-to-scale-and-maintain-legacy-css-with-sass-and-smacss/)
  * [Objects in Space - A style-guide for modular SASS development using SMACSS and BEM.](https://medium.com/objects-in-space/f6f404727)
