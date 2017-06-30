# scss-grid
Very flexible and easy to use SCSS gridsystem.

## Setup
Simply change the _grid-settings.scss file to your likings. Here you can set the total width, columns, gutter (room between columns). For flexibility reasons, I don't use gutters.

## Examples and how to use coming soon
I've set this repo up pretty quick, just for sharing. I will soon provide it with all sorts of examples. For now, know that you can use it in your scss-files like so:

``` scss

.row{
    @include row(); //use this for every new row on the grid. Note, this is not required, you can also use columns for elements outside the grid.
}

.columnTenWide{
    @include column(10); //calculates with grid _grid-settings.scss
}

.columnPushed{
    @include column(10);   
    @include push(4);
}

.columnExactlyHalf{
    @include column(1,2); //takes 2 as total amount of columns. Expecially usefull for subgrids. More about this soon
}
```

You HTML can be like this:
``` html

<div class="content">
    <div class="row">
        <div class="columnTenWide">This column is 10 wide</div>
        <div class="columnPushed">This column is 10 wide and pushed 4 spaces</div>
    </div>
    <div class="row">
        <div class="columnExactlyHalf">This column is exactly half of the parent</div>
        <div class="columnExactlyHalf">This column is exactly half of the parent</div>
    </div>
</div>

```