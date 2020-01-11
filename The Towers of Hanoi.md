## The Towers of Hanoi

> The equipment includes three posts and a set of discs of various diameters with holes in their centers. The setup stacks all of the discs on the source post with smaller discs on top of larger discs. The goal is to move the stack to the destination post by moving once disc at a time to another post, never placing a larger disc on a smaller disc.

### JavaScript
```javascript
var hanoi = function hanoi(discs, src, aux, dst) {
    if (discs > 0) {
        hanoi(discs - 1, src, dst, aux);
        console.log(`Move disc ${discs} from ${src} to ${dst}`);
        hanoi(discs - 1, aux, src, dst);
    }
}
```