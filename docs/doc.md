PubPub Design Guide
================
Travis Rich, Thariq Shihipar, Andrew Johnson

<h2 id="philosophy">Introduction</h2>

<div class="overview">This document is a living design guideline for [PubPub](http://www.pubpub.org/). Use it as a guideline for creating a great publication experience across browsers, users and contexts.</div>

<div class="principles">
    <div class="principle-text">
      <h4>Information Everywhere</h4>
      <p>We present the great thinking and research on PubPub through designs that can be easily distributed and open sourced.</p>
    </div>
    <div class="principle-image">
      ![](images/pubpubicons-02.png)
    </div>
</div>

<div class="principles second">
    <div class="principle-image">
      ![](images/pubpubicons-03.png)
    </div>
    <div class="principle-text">
      <h4>Share Systems</h4>
      <p>We create consistent reusable styles and components for cohesive and collaborative experiences.</p>
    </div>
</div>

<div class="principles">
    <div class="principle-text">
      <h4>Encourage Understanding</h4>
      <p>We communicate and support the message of our users’ content by providing great editorial/publication design for everyone.</p>
    </div>
    <div class="principle-image">
      ![](images/pubpubicons-04.png)
    </div>
</div>

<h2 id="pagestructure">Typography</h2>

Typography is the backbone of Pubpub’s design and supports content / maintains hierarchy. Sizes assume a body <code>font-size</code> of <code>16px</code>. <code>Rem</code> values inherit font size directly from the root element. Use something like [pixrem](https://www.npmjs.com/package/gulp-pixrem) if you need to support IE 10 and down.

#### Global Interface Typography

Typography across the PubPub interface in general makes heavy use of the functional and economic Clear Sans. It’s limited to a few select styles. 

<div class="fonts">
    <div class="font clearsans-bold">
        <div class="font-use">Titles</div><div class="font-size">1.9rem</div><div class="font-family">Clear Sans Bold</div>
    </div>
    <div class="font clearsans-light">
        <div class="font-use">Sub Nav / Titles</div><div class="font-size">1.2rem</div><div class="font-family">Clear Sans Light</div>
    </div>
    <div class="font clearsans">
        <div class="font-use">Base Font Size</div><div class="font-size">1rem</div><div class="font-family">Clear Sans</div>
    </div>
    <div class="font clearsans">
        <div class="font-use">Small Text</div><div class="font-size">.9rem</div><div class="font-family">Clear Sans</div>
    </div>
</div>


#### The Publication View

For publications, PubPub takes advantage of the legibile / readable typeface [Yrsa](https://www.rosettatype.com/blog/2015/09/01/Introducing-Yrsa) which also has a wide range of European language support. It’s paired beautifully with the utilitarian Clear Sans:

<div class="example-container">
    <div class="example-h1">A Prehistory of the Anti-Disciplinary: Cybernetics</div>
    <p class="example-paragraph">Although the new technologies and tools diminishing costs driven by the Internet and Moore’s Law makes antidisciplinary work increasingly possible, it’s not exactly a new idea.</p>

    <p class="example-paragraph">Driven less by the diminishing costs, but rather by a whole set of enabling technologies and tools, a similar movement was occurring in the 1940s and 1950s where a variety of fields began to converge. Applications from ballistic missile control to understanding how biological systems regulated movement brought engineers, designers, scientists, mathematicians, sociologists, philosophers, linguists, psychologists and thinkers from a variety of fields together to begin to understand systems and feedback loops as a way to both comprehend and design complex systems. This type of cross-disciplinary study of systems was termed “cybernetics.”
    </p>
</div>

PubPub uses a system across it’s publication view to maintain clarity.

<div class="fonts publication-view">
    <div class="font yrsa-bold">
        <div class="font-use">Title</div><div class="font-size">3.5em</div><div class="font-family">Yrsa Bold</div>
    </div>
    <div class="font clearsans-light">
        <div class="font-use">h1</div><div class="font-size">2.2rem</div><div class="font-family">Clear Sans Light</div>
    </div>
    <div class="font clearsans-light">
        <div class="font-use">h2</div><div class="font-size">1.9rem</div><div class="font-family">Clear Sans Light</div>
    </div>
    <div class="font clearsans-bold">
        <div class="font-use">h3</div><div class="font-size">1.6rem</div><div class="font-family">Clear Sans Bold</div>
    </div>
    <div class="font clearsans-bold">
        <div class="font-use">h4</div><div class="font-size">1.2rem</div><div class="font-family">Clear Sans Bold</div>
    </div>
    <div class="font clearsans-bold">
        <div class="font-use">h5</div><div class="font-size">1rem</div><div class="font-family">Clear Sans Bold</div>
    </div>
    <div class="font yrsa">
        <div class="font-use">Text</div><div class="font-size">1.35rem</div><div class="font-family">Yrsa</div>
    </div>
    <div class="font yrsa-bold">
        <div class="font-use">Text Bold</div><div class="font-size">1.35rem</div><div class="font-family">Yrsa</div>
    </div>
    <div class="font merriweather-italic">
        <div class="font-use">Text Italic</div><div class="font-size">.95rem</div><div class="font-family">Merriweather</div>
    </div>
    <div class="font clearsans">
        <div class="font-use">Text Comments</div><div class="font-size">1rem</div><div class="font-family">Clear Sans</div>
    </div>

</div>

#### The Editor View

For writting in Markdown, PubPub utilizes the monospace typeface Inconsolata.

<div class="fonts editor-view">
    <div class="font inconsolata-bold">
        <div class="font-use">Title</div><div class="font-size">1.8rem</div><div class="font-family">Inconsolata</div>
    </div>
    <div class="font inconsolata">
        <div class="font-use">Text</div><div class="font-size">1.1rem</div><div class="font-family">Inconsolata</div>
    </div>
</div>

<br/>

#### Font Stack

The font stack should be defined as such:

<pre>
.foo {
    font-family: 'Yrsa', Georgia, serif;
}
.bar {
    font-family: 'ClearSans', Helvetica Neue, Arial, sans-serif;
}
</pre>

#### OpenType Features

The CSS property <code><a href="https://developer.mozilla.org/en-US/docs/Web/CSS/font-variant">Font feature settings</a></code> should be used wherever possible to enable kerning. Avoid setting the CSS property <code><a href="https://developer.mozilla.org/en-US/docs/Web/CSS/text-rendering" target="0">text-rendering</a></code> globally – it <a href="http://bocoup.com/weblog/text-rendering/">comes with some performance tradeoffs.</a>

<pre>
* {
  font-kerning: normal;
  font-variant-ligatures: common-ligatures;
}
</pre>

<h4>Font Rendering</h4>

The CSS property <code>-webkit-font-smoothing: antialiased</code> should only be applied on type set <em>at or above 1em</em> or on light type on dark backgrounds to ensure clear rendering.

<pre>
.foo-bar {
  -webkit-font-smoothing: antialiased
}
</pre>

<h2 id="pagestructure">Color</h2>

PubPub makes use of a largely grayscale, subtle color palette across its interface to keep information clear. Longform text should always be <code>color: #2C2A2B</code>.

<h4>Hex Colors</h4>

<div class="colors">
    <div class="dark-gray">
        #2C2A2B
    </div>
    <div class="medium-dark-gray">
        #363736
    </div>
    <div class="medium-gray">
        #58585B
    </div>
    <div class="medium-light-gray">
        #808284
    </div>
    <div class="light-gray">
        #BBBDC0
    </div>
    <div class="background-gray">
        #F3F3F4
    </div>
</div>

<h4>Color Classes</h4>

<pre>
.dark-gray {
    background-color: #2C2A2B;
}
.medium-dark-gray {
    background-color: #363736;
}
.medium-gray {
    background-color: #58585B;
}
.medium-light-gray {
    background-color: #BBBDC0;
}
.light-gray {
    background-color: #808284;
}
.background-gray {
    background-color: #F3F3F4;
}
</pre>

<h2 id="pagestructure">Buttons</h2>

Like people, buttons come in different shapes and sizes and there's a reason for every one. Use the appropriate one for the job to maintain hierarchy and guide users through their tasks.

<h4 id="">Button Base Class</h4>

These should be used in almost every case.

<a href="#" class="button">Show Me Science</a>  

<pre>
.button {
  display: inline-block;
  font-family: 'ClearSans', Helvetica Neue, Arial, sans-serif;
  font-size: 1rem;
  font-weight: 100;
  border: solid 2px #58585B;
  color: #58585B;
  padding: .9em 1.8em;
  transition: all .2s ease-out;
}
.button:hover {
  border: solid 2px #2C2A2B;
  background-color: #2C2A2B;
  color: #FEFEFE;
}
</pre>

<h4 id="">Button Modifiers</h4>

These should be used only where functionality is secondary or tertiary/quaternary respectively, in nature.

<a href="#" class="button medium">Submit</a>

<pre>
.button.medium {
    padding: .45em .9em .6em .9em;
    border-radius: .1rem;
}
</pre>

<a href="#" class="button small">Request Review</a> 

<pre>
.button.small {
  font-size: .9em;
  border: solid 1px #58585B;
  padding: .15em .8em .2em .8em;
  border-radius: .1rem;
}
.button.small:hover {
  border: solid 1px #2C2A2B;
}
</pre>



<h2 id="changelog">Change Log</h2>

Version 0.0.2 – April 13th

Version 0.0.1 – March 29th
