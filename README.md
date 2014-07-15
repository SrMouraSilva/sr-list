<sr-list>
=========

An web component list-group abstraction with pre-defined handling methods

About
------
Em algum momento você já precisou [de um menu vertical simples](http://getbootstrap.com/components/#list-group), ou uma [lista passo a passo](http://www.polymer-project.org/#learn).
Quando é necessário em um webapp, temos que por vezes adicionar, remover, desabilitar, atualizar dinamicamente estes itens, e para fazer algo minimamente aproveitável, gasta-se um tempo abstraindo e criando código.

A ideia do <sr-list> é justamente dar o básico do que já precisamos há tempos de uma forma amigável e customizável.

Demo
------
[Online demo in here](https://donnot-iberia.codio.io/index.html)

Support
----------
Firefox, Chrome (linux)
Chrome (windows): Impementing

How to use
----------

### Marcation
```hmtl
<h2> As list-group (type="vertical") </h2>
	<aside role="complementary">

	<sr-list type="vertical">
		<sr-item>Normal</sr-item>
		<sr-item selected>Selected</sr-item>
		<sr-item disabled>Disabled</sr-item>
		<sr-item separator></sr-item>
		<sr-item icon="icon.png">With icon</sr-item>
		<sr-item icon-class="fa-plus">With icon-class</sr-item>
		<sr-item separator></sr-item>
		<sr-item href="index.html">With href (please, mouseover me)</sr-item>
	</sr-list>

	</aside>

	<h2> As menu (type="horizontal") </h2>
	<nav role="navigation">

	<sr-list type="horizontal">
		<sr-item icon="icon.png">A menu item</sr-item>
		<sr-item separator></sr-item>
		<sr-item href="javascript:console.log('clicked')">Logout</sr-item>
	</sr-list>

	</nav>

```
__Note__: strikethrough -> not implemented

#### Attributes
##### sr-list
* ~~type~~:
  - ~~Values: "vertical", "horizontal"~~ (buggy)
* disable: Disable it

##### sr-item
* icon: Add a icon image in left of the text
* ~~icon-class: Class of image src. [Like as Font Awesome](http://fortawesome.github.io/Font-Awesome/)~~
* disabled: Disable it
* selected: Select it
* href: As a[type=href] attribute. Use to redirect page or add javascript methods
* separator: Separator divider (only sr-menu[horizontal])

#### Handling
##### sr-list
* add(label, attributes, position) Add a sr-item in the menu
  - label:      String     Label of list item
  - attributes: Object     {"attribute-name": "value"}
  - position:   Int        Position where item will be added.
  - position:   undefined  Last position
* get(index) Return the item with this 'index'
  - index: Int  index of item
* getItems() Return all children items
* remove(index) Remove item in the index position
  - index: Int  index position. -1 as last
* sr-item getSelected() Return the first element with state seleted
* [sr-item's] getSelectedAll() Return all the elements with state seleted
* disable() Change state to disabled
* disable(state) Change state to enabled
  - state: undefined  Change state to disabled
  - state: boolean    Change state to enabled


##### sr-item
* boolena isSelected() return boolean
* select(state) Change state to select
  - state: undefined  Change state to selected
  - state: boolean    Change state to unselected
* boolean isDisabled() return boolean
* disable() Change state to disabled
* disable(state) Change state to enabled
  - state: undefined  Change state to disabled
  - state: boolean    Change state to enabled
* int getIndex() Return the index of the element. -1
* int getIndex() Return -1: Could not be found


#### Customing desing
You can edit style! Try:

```
sr-list {
	background-color:
}
sr-item {
	background-color:
}
sr-item[selected] {
	background-color:
}
sr-item[selected]:hover {
	background-color:
}
sr-item[disabled] {
	background-color:
}
sr-item[selected][disabled] {
	background-color:
}
sr-item:hover {
	background-color:
}

/* Buggy */
sr-item:focus {
	background-color:
}
sr-item:active {
	background-color:
}
```