# CSS

Bootstrap link comes before CSS script.

element.class - selects by class

direct child example - 
plate > apple
> means direct child

pseudo selectors -
element:first-child
element element:only-child selects only the child of the element

element:nth-child(#) - selects by order in another element
element:nth-last-child(#) - counts from the back

element:first-of-type - selects by first of type
element:nth-of-type(even/odd) - can select only evens and odds

plate:nth-of-type(2n + 3) - selects every 2 plates starting at 3

object-fit: contain - will keep image from overflowing. it will stay within box

image-fit {
    width: x;
    height: y;
    object-fit: contain;
}
        / \
         |    can tweak this a bunch to get the right image size for image cards using row and col ⭐⭐⭐

image-crop {
    width: x;
    height: y;
    object-fit: cover;
    object-position: value;
}
        / \
         |    can tweak this a bunch to get the right image crop for image cards using row and col ⭐⭐⭐

background-size: cover; makes the image cover the whole div

img container {
    background-image: url
    height: 250vh;
} ⭐⭐⭐

check out the filter property later! ⭐

text-center on div will center image ⭐⭐

Dont text center paragraphs.

Text center header and then text-start paragraph