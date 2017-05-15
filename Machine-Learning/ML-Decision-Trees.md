# Decision Trees

## Intuition

**CART: Classification and Regression Trees**

We speak about both types, but for now - focus on regression trees.

Regression trees are a bit more complex than classification trees.

Imagine a scatter plot with two IV and we are predicting an DV y (which you wouldn't be able to see on the chart). Essentially the DV would sit on the z axis.

Once you run the regression decision tree algorithm, the scatter plot will be split up into segments.

For example, x1 might be split at 20. Another split may happen for x2 at 170, 200 etc.

The question, are the splits adding value to way we want to group our points?

Each split itself is known as a leaf.

The algorithm can handle mathematical issues and we can focus on the practical element of the algorithm.

**Splitting**

If we split `x[1] < 20`, we have two options (y/N). If we then split `x[2] < 170`, we add a child node to `x[1] < 20` that checks y/N. If we then set ``x[2] < 200`.

After having a two child tree, if we set `x[1] < 40` such that `x[1] < 20` is not true and `x[2] < 170` is true, we can then set `x[1] < 40` as the child to `x[2] < 170`.

Once we start this tree, what do we populate into those boxes? Well, we decide how we predict `y` with a new observation added to the plane x[1] and x[2].

Key note: `Adding splits adds information`.

What we do is that for each terminal leaf, we take the average and assign the value that we give to any new element that falls into that leaf.

Now, if we have a new value, we check the decision tree where it falls and then assign the new element the value of where it falls as a prediction.