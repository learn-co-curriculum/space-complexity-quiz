# Day 2: Space Complexity Quiz

1. Multiple-choice

Calculate the space complexity for the following code. We've included both JS and Ruby for the same function.

<h3>JavaScript</h3>
<pre>
<code>
function shallowCopy(array) {
  const copy = [];

  array.forEach(el => {
    copy.push(el);
  });
}

return copy;
</code>
</pre>

<h3>Ruby</h3>
<pre>
<code>
def shallow_copy(array)
  copy = []

  array.each { |el| copy << el }

  copy
end
</code>
</pre>

- O(n)
  - Correct! The input array is the weakest link and the space required grows proportionally with the size of the array.
- O(1)
  - Not quite. This means that the required space would be the same regardless of the length of the array, which is not the case. The input array could be of any length.
- O(2n)
  - Almost. Remember that for Big O notation, we drop the coefficients.
- O(n<sup>2</sup>)
  - Not quite. The space required does not grow at this high of a rate.
- I don't know
  - Take some time to study and practice. You'll get there!

2. Multiple-choice

Calculate the space complexity for the following code. We've included both JS and Ruby for the same function.

<h3>JavaScript</h3>
<pre>
<code>
// inputs will be integers

function speakTotal(a, b) {
  const total = a + b;

  return `${a} + ${b} is ${total}`;
}
</code>
</pre>

<h3>Ruby</h3>
<pre>
<code>
# inputs will be integers

def speak_total(a, b)
  total = a + b

  "#{a} + #{b} is #{total}"
end
</code>
</pre>

- O(1)
  - Exactly! It doesn't matter which integers <code>a</code> and <code>b</code> are, the space required for this function never grows.
- O(n)
  - Not quite. Is there a difference in the required space if <code>a</code> is 5 and <code>b</code> is 10, or <code>a</code> is 20 and <code>b</code> is 30?
- O(3)
  - Not quite. Remember, we need to simplify our answer for Big O. Which of the common notations is the better choice?
- I don't know
  - Take some time to study and practice. You'll get there!

3. Multiple-choice

Calculate the space complexity for the following code. We've included both JS and Ruby for the same function.

<h3>JavaScript</h3>
<pre>
<code>
function makeExtras(string) {
	const charArray = string.split('');
  const extrasArray = [];
  
  for (let i = 0; i < string.length; ++i) {
  	for (const char of string) {
    	extrasArray.push(char);
    }
  }
  
  return extrasArray.join('');
}
</code>
</pre>

<h3>Ruby</h3>
<pre>
<code>
def make_extras(string)
  extras_string = ''

  string.length.times do
    string.chars { |char| extras_string += char }
  end

  extras_string
end
</code>
</pre>

- O(n<sup>2</sup>)
  - Whoooo! The returned string is the weakest link and its final size is the square of the input.
- O(n)
  - Not quite. How long is the returned string if the input is 1 character? What if the input is 3 characters?
- O(log n)
  - Not quite. This algorithm is definitely going to need more space. The input is never being divided here.
- I don't know
  - Take some time to study and practice. You'll get there!