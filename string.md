# `String`
We've already met the `String` class a few times, but here are some handy
methods to try:
## Methods
### `+`
`String`s can be added together
<iframe frameborder="0" width="100%" height="600px" src="https://repl.it/student_embed/assignment/3054739/1cc4addd0db0fc551a3150b705aec540"></iframe>

<iframe frameborder="0" width="100%" height="600px" src="https://repl.it/student_embed/assignment/3054821/8ae9caede166ee39391c41fd99c4695c"></iframe>

### `*`
`String`s can be multiplied, but the order matters
<iframe frameborder="0" width="100%" height="600px" src="https://repl.it/student_embed/assignment/3055223/0d5863acb6b355c53573fb78e13c0107"></iframe>

<iframe frameborder="0" width="100%" height="600px" src="https://repl.it/student_embed/assignment/3055761/b8091d3eabe958cc55c0dd0d0845ec75"></iframe>
### `upcase`
<iframe frameborder="0" width="100%" height="600px" src="https://repl.it/student_embed/assignment/3055582/03f0b9912e42550cc2f5871b06e7a4c7"></iframe>

### `downcase`
<iframe frameborder="0" width="100%" height="600px" src="https://repl.it/student_embed/assignment/3055585/368b0578faa55ae7f025a9808e51d885"></iframe>

### `swapcase`
<iframe frameborder="0" width="100%" height="600px" src="https://repl.it/student_embed/assignment/3055713/54ad2cc82183a62b5d62b5c61d14dbe5"></iframe>

<iframe frameborder="0" width="100%" height="600px" src="https://repl.it/student_embed/assignment/3054730/4e44347737416ad6d635474a0e3369f1"></iframe>

### `reverse`
<iframe frameborder="0" width="100%" height="600px" src="https://repl.it/student_embed/assignment/3054840/6d6e7c37386f001d85ca9a6949c722c7"></iframe>

<iframe frameborder="0" width="100%" height="600px" src="https://repl.it/student_embed/assignment/3054730/4e44347737416ad6d635474a0e3369f1"></iframe>

### `length`
<iframe frameborder="0" width="100%" height="600px" src="https://repl.it/student_embed/assignment/3054853/4064e68cc52741fb36ad36bcd0f97b81"></iframe>

### `chomp`
<iframe frameborder="0" width="100%" height="600px" src="https://repl.it/student_embed/assignment/3055034/4d88518a794de6d0b8b0bdbd50e2012d"></iframe>

<iframe frameborder="0" width="100%" height="600px" src="https://repl.it/student_embed/assignment/3055768/5eff4e7c735dc2a2821e719a87c82c36"></iframe>

### `gsub`
<iframe frameborder="0" width="100%" height="600px" src="https://repl.it/student_embed/assignment/3055040/35043a91cfe78e61421921e1f0a437ce"></iframe>

<iframe frameborder="0" width="100%" height="600px" src="https://repl.it/student_embed/assignment/3055200/37255ba7d887c35597b69abd8c7cdc9d"></iframe>

### `to_i`
Sometimes you have a string that contains a number, usually input from a user,
and want to do math on it. `to_i` will attempt to convert a `String` object into
an `Integer` object.
<iframe frameborder="0" width="100%" height="600px" src="https://repl.it/student_embed/assignment/3055570/9e0d4bf6a7c462730fb6af44c352bc36"></iframe>

### `strip`
`strip` removes all leading and trailing whitespace
<iframe frameborder="0" width="100%" height="600px" src="https://repl.it/student_embed/assignment/3055572/55951eda552514e8e7ec0b70dcbaf8c9"></iframe>

<iframe frameborder="0" width="100%" height="600px" src="https://repl.it/student_embed/assignment/3056024/e3e79ed5afa47389e0299abf09e3369f"></iframe>

### `gsub(/\s+/, "")`
This is an advanced technique that removes all whitespace
### `gsub(/[^a-z0-9\s]/i, "")`
This is an advanced technique that removes everything except alphanumerics and
whitespace
### `capitalize`
<iframe frameborder="0" width="100%" height="600px" src="https://repl.it/student_embed/assignment/3055716/b14358704094311fe491d83c5834474e"></iframe>

### `gsub(/[^a-z0-9\s]/i, "").strip`

### `split`
This produces an Array, which you can read about [here.](array.md)
<iframe frameborder="0" width="100%" height="600px" src="https://repl.it/student_embed/assignment/3056028/5081a3ff7359af302bb4574448801dda"></iframe>

### `split.count`
Arrays are lists, and can be counted.

<iframe frameborder="0" width="100%" height="600px" src="https://repl.it/student_embed/assignment/3056031/c3f32f8021d7a4eac0adaaf47baf45be"></iframe>

## More
We spend a lot of time composing strings of output for our users, so let's see a
few more examples. Try this:

```ruby
message = "Your lucky number for today is " + rand(100) + "."
```

You'll see that Ruby gets confused, because we are trying to add an integer to a
string and it doesn't feel comfortable with that.

The solution is to tell the integer to convert itself to a string first:

```ruby
message = "Your lucky number for today is " + rand(100).to_s + "."
```

The above technique for composing strings, adding them together with `+`, is
called **string concatenation**.

There's another technique for composing strings that I personally find a bit
easier; it's called **string interpolation**. It goes like this:

```ruby
message = "Your lucky number for today is #{rand(100)}."
```

 Basically, inside the string, you place `#{}` where you eventually want your
value to go. Inside the curly braces, you can write any Ruby expression without
worrying about whether it is a string or not. The expression will be evaluated,
converted to a string, and added to the string right in that spot. You can
interpolate as many expressions as you want into a single string. Pretty neat!

 If you find interpolation confusing, feel free to just use concatenation.