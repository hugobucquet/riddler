## Can you make room for goats?

*A goat tower has 10 floors, each of which can accommodate a single goat. Ten goats approach the tower, and each goat has its own (random) preference of floor. Multiple goats can prefer the same floor*.

*One by one, each goat walks up the tower to its preferred room. If the floor is empty, the goat will make itself at home. But if the floor is already occupied by another goat, then it will keep going up until it finds the next empty floor, which it will occupy. But if it does not find any empty floors, the goat will be stuck on the roof of the tower.*

*What is the probability that all 10 goats will have their own floor, meaning no goat is left stranded on the roof of the tower?*

For each goat $g$, let $f(g)$ be the random varaible corresponding to its preferred floor.

It is easy to see that each goat has its own floor iff <br>
$$ \forall i \in [1,10], \#\{g, f(g) > i\} \leq 10 -i$$

By symmetry, for each event that satisfies the condition above, there is an event of equal probability that doesn't satisfy it where each goat $g$ has a preferred floor of  $11 - f(g)$.

We only left out the case where each goat prefers a different floor, where switching the floors like above still results in a situation where each goat has its own floor.

Thus, the probability that each goat ends up on its own floor in $1/2 + P(\#\{f(g), g \in GOAT\} = 10)$.

Because, $\#\{f(g), g \in GOAT\} = 10!$, $P(\#\{f(g), g \in GOAT\} = 10) = 10!/10^{10}$.

Thus, our final answer is $$\boxed{1/2 + 10!/10^{10}}$$



