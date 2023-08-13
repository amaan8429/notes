CSS NOTES

<h3>Responsiveness</h3>

em

em is about size of the text according to the size of the parent

<div class="parent">
  <div class="child1"></div>
  <div class="child2"></div>
  <div class="child3"></div>
</div>

.parent {
font-size: 30px;
}
.child1 {
font-size: 1em;
}
.child2 {
font-size: 1.5em;
}
.child3 {
font-size: 2em;
}

now in this example = 1em in child1 means 30px whereas in child2 fontsize is 45px (1.5em) ,1.5 of parent ka font size

rem

1 rem is 16px
still some doubt ,will update later

px

px is fixed
koi cheez pixel me bna dia to uska siza fix ho jata hai ,phir chahe screen shrink kare koi fark nhi padega. size will remAin constant

%

% me child me agar percent de dia to vo apne app to parent ke percent ke hisab se adjust karne lagega

<div class="parent">
  <div class="child1"></div>
</div>

.parent {
width: 300px;
height: 500px;
}
.child1 {
width: 30%;
height: 50%;
}

to child1 ka width ka width hoga 100px aur height 150px
isme parent banana dhyan rakhna

vw

viewport width
laptop me vw is more and vh is less and in mobiles vh is more and vw is less.

ab ye depend karega on width of the viewport

<div class="main">
  
</div>

.main {
width: 4vw;
}

if you change the height ,it wont affect the sizes because vw use kia hai

vh
viewport height
laptop me vw is more and vh is less and in mobiles vh is more and vw is less.

ab ye depend karega on height of the viewport

<div class="main">
  hello
</div>

.main {
font-size: 4vh;
}

if you change the size ,it wont affect the sizes because vh use kia hai

vmax

isme it will depend on max viewport
let us consider the case of laptop vw is max so it will change the size of the text accoring to the size of vw and still start shrinking as we make the viewport smaller but one point it will stop working (meaning it will stop the further shrinking of the text).
what is this stage = this stage will come when vh will no longer be the vmax of the screen.
vh will become bigger at some point while shrinking . at that exact moment it will stop depending on the vw and and start depending on the vh because vh is max now.

basically , it depends on maximum viewport of the screen ,agar max viewport vh hai to vh p depend karega but if the time comes when vh becomes maximum , it will start depending on the vh .

vmin
let us consider the same case of a laptop
basically , it depends on minimum viewport of the screen ,agar min viewport vh hai to vh p depend karega but if the time comes when vw becomes minimum , it will start depending on the vw .

FLEXBOX ==

.parent class denotes the following properties are applied to parent class

.parent {
display: flex;
flex-direction: row;  
 flex-direction: column;
flex-direction: is used to selec the main axis;
justify-content:center;flex-start; flex-end;space-evenly;space-between;start;end;space-around;
justify-content: use to align items in the main axis
align-items: ; use to align-items in the cross axis
flex-wrap is used to wrap the stuff when screen size stsrts becoming small.they use diffirernt lies when there is no more space available
when flex-wrap is used a new property is unlocked which is align:content which is used to align items on the cross axis when text is wrapped . it only works when wrapping is happened.gap:1em;this is used to give gap between the children
}

.child1{
flex-grow:1;this item will take all the space left after giving the spaces to child2 and 3
flex-shrink:4;this item will shrink at faster rate than other children.if i set it to 0 , the item will refuse to shrink.
flex-basis:300px;it overrides the initial width given to the child.
Nobody uses these properties instead people use a shortcut.
flex: 1,4,300px;this will set the above three properties at once.
align-self:this will override the align-item property set to the parent but just for this child.
}

Media Queries
Options
max-width
min-width
max-height
min-height

Syntax=
@media (max-width:300px) {
these new queries will only work till 300px screen width.
maximum itna width bas.
}
@media (min-width:300px) {
these new queries will only work after 300px screen width.
minimum itna width chahiye.
}
