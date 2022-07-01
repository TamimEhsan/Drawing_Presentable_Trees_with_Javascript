# Drawing Presentable Trees

This is the javascript version of the original work [Drawing Presentable Trees](https://llimllib.github.io/pymag-trees/) which was written in python by Bill Mill. You can find the whole procedure of how this works there.
I used this to create different tree algorithm visualizer which can be found here in [Algorithm Visualizer](https://github.com/TamimEhsan/AlgorithmVisualizer)

## Original motivation by author

When I needed to draw some trees for a project I was doing, I assumed  that there would be a classic, easy algorithm for drawing neat trees.  What I found instead was much more interesting: not only is tree layout  an NP-complete problem[1](https://llimllib.github.io/pymag-trees/#foot1), but there is a long and interesting history behind tree-drawing  algorithms. I will use the history of tree drawing algorithms to  introduce central concepts one at a time, using each of them to build up to a complete O(n) algorithm for drawing attractive diagrams of trees.

## How to use

Create a tree like this from bottom up

```javascript
let ll = new Tree("ll",[]);
let lr = new Tree("lr",[]);
let rr = new Tree("rr",[]);
let rl = new Tree("rl",[]);
let l = new Tree("l",[ll,lr]);
let r = new Tree("r",[rl,rr]);
let root = new Tree("root",[l,r] );
```

here `root` has two children  `l` and `r`. l has two children `ll` and `lr`. `r` has two children `rl` and `rr`

Then call `buchheim` with `root` as parameter

```javascript
let tree = buchheim(root);
```



## Output

The console output generated when `dfs(tree)` is called is

![](Assets\console.jpg)

And this can be used to create a tree like this

![](Assets\tree.jpg)
