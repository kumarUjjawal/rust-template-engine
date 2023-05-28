# A Simple Template Engine Written in Rust

## Here is how it works:

1. The template string is fed to the parser. The template string in our example is
<p> Welcome {{name}} </p>.

2. The parser first determines the type of template string, which is called tokenizing.
Let's consider three types of tokens – if tags, for tags, and template variables. In
this example, a token of type template variable is generated (if the template string
contains a static literal, it is written to the HTML output without any changes).

3. Then the template string is parsed into a static literal, Welcome, and a template
variable {{name}}.

4. The outputs of the parser (from steps 2 and 3) are passed to the HTML generator.

5. Data from a data source is passed as context by the template engine to the generator.

6. The parsed token and strings (from steps 2 and 3) are combined with the context
data (from step 5) to produce the result string, which is written to the output
HTML file.

## To Run:

```cargo run```

## Arguments
```<h2> Hello </h2>```
```<p> My name is {{name}} </p> or <p> I live in {{city}} </p>```
> Expected output: My name is Ujjawal I live in NewDelhi

## ToDo

1. Implement ForTag
2. Implement IfTag
3. Add support for two variables on a single line html
