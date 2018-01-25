CSSGrid by WesBos
--
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


> Note : practicing CSS Grid in Firefox Developer Edition using VSCode with Emmet abbrevation.