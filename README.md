<sr-list>
=========

An web component list-group abstraction with pre-defined handling methods

About
------
Em algum momento você já precisou [de um menu vertical simples](http://getbootstrap.com/components/#list-group), ou uma [lista passo a passo](http://www.polymer-project.org/#learn).
Quando é necessário em um webapp, temos que por vezes adicionar, remover, desabilitar, atualizar dinamicamente estes itens, e para fazer algo minimamente aproveitável, gasta-se um tempo abstraindo e criando código.

A ideia do <sr-list> é justamente dar o básico do que já precisamos há tempos de uma forma amigável e customizável.

Support
----------
Currently only in Chrome :/

How to use
----------

### Marcation
```hmtl
<h2> As list-group (type="vertical") </h2>
	<aside role="complementary">

	<sr-list type="vertical">
		<sr-item>Normal</sr-item>
		<sr-item selected="selected">Selected</sr-item>
		<sr-item disabled="disabled">Disabled</sr-item>
		<sr-item separator="separator"></sr-item>
		<sr-item icon="icon.png">With icon</sr-item>
		<sr-item icon-class="fa-plus">With icon-class</sr-item>
		<sr-item separator="separator"></sr-item>
		<sr-item href="index.html">With href (please, mouseover me)</sr-item>
	</sr-list>

	</aside>

	<h2> As menu (type="horizontal") </h2>
	<nav role="navigation">

	<sr-list type="horizontal">
		<sr-item icon="icon.png">A menu item</sr-item>
		<sr-item separator="separator"></sr-item>
		<sr-item href="javascript:console.log('clicked')">Logout</sr-item>
	</sr-list>

	</nav>

```
__Note__: strikethrough -> not implemented

#### Attributes
##### sr-list
* ~~type~~:
* * ~~Values: "vertical", "horizontal"~~

##### sr-item
* icon: Add a icon image in left of the text
* ~~icon-class: Class of image src. [Like as Font Awesome](http://fortawesome.github.io/Font-Awesome/)~~
* disabled: Disable a list element
* * Value: "disabled"
* selected: Disable a list element
* * Value: "false", "true"
* href: As a[type=href] attribute. Use to redirect page or add javascript methods
* separator: Separator divider

### ~~Handling~~
* ~~add~~
* ~~get~~
* ~~del~~
* ~~set~~
* ~~disable~~
* * ~~Value: "false", "true"~~
* ~~select(int position)~~
* ~~getSelected~~
* ~~getSelectedAll~~


### ~~Customing desing~~
* ~~text color / font~~
* ~~item padding~~
* ~~item :hover :active: focus~~
* ~~item background-color~~
