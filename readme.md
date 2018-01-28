## CSSGrid by WesBos

> Note : practicing CSS Grid in Firefox Developer Edition using VSCode with Emmet abbrevation.

### part6

---

> grid-auto-flow:row

`row` is default value, means all the item we do not explicitly assign them a grid will go to the next row.

Another value is `column`.<br /> It set implicit new item to new column.

### part 7

---

> `fr` unit

`fr` like `1fr` or `2fr` are stand for 1 fraction or 2 fraction, or you can implicitly remember it as `fr-ee`. <br />
`fr` is a unit we used for to determine free space that left after hard coded one (like in `px` of `width`, `height` and `grid-gap`). If we use percentage, the hardcoded one will included, but with `fr`, the browser already take the 100% space taken by hardcoded one like `px` and calculate the rest for use of `fr`. <br />
We can applying `fr` for columns and rows as long as we define the `width` and `height` of the container. <br />
If we combine auto with `fr`, width of auto columns and rows will follow the value inside the item.

### part 8

---

> `repeat()` function

`repeat(a,b)` function in `grid-template-rows (or) grid-template-columns`. <br/>
`repeat(a,b)` function take two params, first `a` for how many times we want to repeat, second `b` for what size do you want for every repeated columns and rows. Params `b` can take more than one size. Example : `grid-template-columns: 50px repeat(2, auto 1fr 5fr 10fr) 300px;`

### part 9

---

> `grid-column:span ...` and `grid-row:span ...` - put it on specific class item

!without `template`. <br/>
put in on specific class of the item. <br/>
Using `span` for combine columns and rows. It take number as parameter. Example : `grid-column:span 4` means it going to combine 4 columns into one columns. But, it not replace the item. It combine the columns space, not the columns it self. So the rest of the item in columns or rows will be implicitly pushed into the next columns or rows. If we put too high number as span params than the columns or rows actually or explicitly define, it will create a implicit columns and row.

### part10

---

> placing git item with track number inside `git-column` and `git-row`

In inspect element, layout tab at firefox devtools, when you tick the show line tool after ticking your container. There is a number show up from 1,2,3 so on. That is track number. <br/>
We can take those number and apply it on `git-column: start/end` and `git-row:start/end`.
example :

```
grid-column: 1/-1;
grid-row: 2/span 3;
```

-1 means we take the entire columns or rows.

### part 11

---

Spanning & Placing Cardio! short exercise.

We can also still use span and combine it with `/`, on the left and on the right side of `/`.

### part 12

---

> `auto-fit` and `auto-fill` most likely have a same feature but..

`auto-fit` allows you to create explicit track at the end of item. <br/>
`auto-fill` allows you to create explicit track at the end of the screen. You can see it more clear with inspecting the element with grid support. Use cases are like

```
grid-template-columns: repeat(auto-fit, 100px);
```

with `auto-fit` setup, you can't move existing item to explicit end space, because there is no more room that created explicitly. <br/> But with `auto-fill`, because it create explicit track at the end of screen, <br/> so if you only have 5 item (look at index12), you can move item to the end of row because there is a room created explicitly by `auto-fill`

### part 13

---

> parameter `minmax(a,b)`

for default you can just use this code

```
grid-template-columns: repeat(auto-fit, minmax(100px, 1fr));
```

this code make your item responsive, not only reduce the size along with screen smaller, but it also push item to new row, this make this incredible XD.

### part 14

---

> `grid-template-areas` in container with it child `grid-area` in each single item.

see the code, fork and try yourself or watch wesbos video. In container 2, we create grid without `grid-template-columns` and `grid-template-rows` by using `grid-template-areas`.

### part 15

---

> assign name to track line use `[]`

`[]` used for name track line, put inside `grid-template-columns` and `grid-template-columns`.
Put between columns and rows, behave like the track line, at the `grid-gap`, then using those name inside `grid-column` and `grid-row` for each item. You can combine more than one name into `[]`.

### part 16

---

> `grid-auto-flow:dense`

by setting to `dense` in container, browser will automaticly fit every item into columns and rows so there will be no blank or hole left in the container.

### part 17

---

> `justify-*` for x axis, `align-*` for y axis.

`justify-items` , `align-items` , `justify-content` , and `align-content`.

> use `place-items` as shorthand of `justify-items` and `align-items`.

### part 18

---

> `order:` property in individual grid item.

Used for determine which one go on the top first. Default value is all 0.

### part 19

---

> project album with `minmax()`, `auto-fit`, grid in grid

copy and run this code with emmet abbrevation, so powerful!

```
.albums>.album*12>img.album__artwork[src="https://sources.splash.com/random/300x300?v=$"]+.album__details>h2{Album Title}+p.album__artist{Artist name}+p.album__desc{Lorem ipsum, dolor sit amet consectetur adipisicing elit. Culpa, laborum}
```

### part 20

---

> borderless grid gallery
> applying HTML,CSS and VanillaJS

### part 21

---

### part 22

---

### part 23

---

### part 24

---

### part 25

---
