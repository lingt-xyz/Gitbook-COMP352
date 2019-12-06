# Traversals

## Question

#### Problem 1 : Draw a tree$$T$$given that:

* A pre-order traversal of $$T$$yields:$$E\ K\ D\ M\ J\ G\ I\ A\ C\ F\ H\ B\ L$$.
* A post-order traversal of$$T$$yields:$$D\ J\ I\ G\ A\ M\ K\ F\ L\ B\ H\ C\ E$$.

{% hint style="info" %}
Divide and conquer
{% endhint %}

1. From `pre-order`, we know$$E$$is the root of$$T$$. This conclusion is consistent with the fact that$$E$$is the last node in `post-order`.
2. From `pre-order`, we know$$K$$is$$E$$'s first child; from `post-order`, we know$$C$$is$$E$$'s last child.
   * If$$E$$has another child which is in-between$$K$$and$$C$$ , it should be$$D$$because of `pre-order`. However,$$D$$is the first node in `post-order`, so$$D$$cannot be in-between$$K$$and$$C$$.
3. Because$$E$$only has a left child$$K$$and a right child$$C$$, we know
   * From `pre-oder`, $$K\ D\ M\ J\ G\ I\ A$$is a left-sub-tree;$$C\ F\ H\ B\ L$$is a right-sub-tree.
   * From `post-order`,$$D\ J\ I\ G\ A\ M\ K$$is a left-sub-tree;$$F\ L\ B\ H\ C$$is a right-sub-tree.

{% hint style="warning" %}
We have conquered the root$$E$$. Now, this problem was divided into two sub-problems:

* Problem 1.1: Draw a tree$$T_1$$where
  * Pre-order traversal yields: $$K\ D\ M\ J\ G\ I\ A$$.
  * Post-order traversal yields:$$D\ J\ I\ G\ A\ M\ K$$.
* Problem 1.2: Draw a tree$$T_2$$where
  * Pre-order traversal yields:$$C\ F\ H\ B\ L$$.
  * Post-order traversal yields:$$F\ L\ B\ H\ C$$.
{% endhint %}





