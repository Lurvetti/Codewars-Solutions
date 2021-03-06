<h3>Directions Reduction - 5 kyu</h3>
https://www.codewars.com/kata/550f22f4d758534c1100025a
<h4>Once upon a time, on a way through the old wild mountainous west,…</h4>
… a man was given directions to go from one point to another. The directions were "NORTH", "SOUTH", "WEST", "EAST". Clearly "NORTH" and "SOUTH" are opposite, "WEST" and "EAST" too.

Going to one direction and coming back the opposite direction right away is a needless effort. Since this is the wild west, with dreadfull weather and not much water, it's important to save yourself some energy, otherwise you might die of thirst!

How I crossed a mountain desert the smart way.
The directions given to the man are, for example, the following (depending on the language):

<p><code>
["NORTH", "SOUTH", "SOUTH", "EAST", "WEST", "NORTH", "WEST"].
</code></p>

or
<p><code>
{ "NORTH", "SOUTH", "SOUTH", "EAST", "WEST", "NORTH", "WEST" };
</code></p>

or

<code>[North, South, South, East, West, North, West]</code>
<p>You can immediatly see that going "NORTH" and immediately "SOUTH" is not reasonable, better stay to the same place! So the task is to give to the man a simplified version of the plan. A better plan in this case is simply:
<code>["WEST"]</code> or <code>{ "WEST" }</code> or <code>[West]</code>
Other examples:
<p>In <code>["NORTH", "SOUTH", "EAST", "WEST"]</code>, the direction "NORTH" + "SOUTH" is going north and coming back right away.
The path becomes <code>["EAST", "WEST"]</code>, now "EAST" and "WEST" annihilate each other, therefore, the final result is <code>[]</code>.

In <code>["NORTH", "EAST", "WEST", "SOUTH", "WEST", "WEST"]</code>, "NORTH" and "SOUTH" are not directly opposite but they become directly opposite after the reduction of "EAST" and "WEST" so the whole path is reducible to <code>["WEST", "WEST"]</code>.

<h4>Task</h4>
Write a function <code>dirReduc</code> which will take an array of strings and returns an array of strings with the needless directions removed (W<->E or S<->N side by side).
<h4>Notes</h4>
Not all paths can be made simpler. The path <code>["NORTH", "WEST", "SOUTH", "EAST"]</code> is not reducible. "NORTH" and "WEST", "WEST" and "SOUTH", "SOUTH" and "EAST" are not directly opposite of each other and can't become such. Hence the result path is itself : <code>["NORTH", "WEST", "SOUTH", "EAST"]</code>.

