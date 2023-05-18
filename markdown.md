# Markdown Files

Whether you write your book's content in Jupyter Notebooks (`.ipynb`) or
in regular markdown files (`.md`), you'll write in the same flavor of markdown
called **MyST Markdown**.
This is a simple file to help you get started and show off some syntax.

## What is MyST?

MyST stands for "Markedly Structured Text". It
is a slight variation on a flavor of markdown called "CommonMark" markdown,
with small syntax extensions to allow you to write **roles** and **directives**
in the Sphinx ecosystem.

For more about MyST, see [the MyST Markdown Overview](https://jupyterbook.org/content/myst.html).

## Sample Roles and Directives

Roles and directives are two of the most powerful tools in Jupyter Book. They
are kind of like functions, but written in a markup language. They both
serve a similar purpose, but **roles are written in one line**, whereas
**directives span many lines**. They both accept different kinds of inputs,
and what they do with those inputs depends on the specific role or directive
that is being called.

Here is a "note" directive:

```{note}
Here is a note
```

It will be rendered in a special box when you build your book.

Here is an inline directive to refer to a document: {doc}`markdown-notebooks`.


## Citations

You can also cite references that are stored in a `bibtex` file. For example,
the following syntax: `` {cite}`holdgraf_evidence_2014` `` will render like
this: {cite}`holdgraf_evidence_2014`.

Moreover, you can insert a bibliography into your page with this syntax:
The `{bibliography}` directive must be used for all the `{cite}` roles to
render properly.
For example, if the references for your book are stored in `references.bib`,
then the bibliography is inserted with:

```{bibliography}
```

## Learn more

This is just a simple starter to get you started.
You can learn a lot more at [jupyterbook.org](https://jupyterbook.org).


```{code-block} python
# :lineno-start: 10
# :emphasize-lines: 1, 3

a = 2
print('my 1st line')
print(f'my {a}nd line')
```

Feel free to go through the contents.

````{margin}
```{note}
Here's my note!
```
````

```{note}
Here is a note
```

```{admonition} My markdown link
Here is [markdown link syntax](https://jupyter.org)
```
nested 
````{note}
The next info should be nested
```{warning}
Here's my warning
```
````
Since Pythagoras, we know that {math}`a^2 + b^2 = c^2`

```{math} e^{i\pi} + 1 = 0
:label: euler
```

Euler's identity, equation {math:numref}`euler`, was elected one of the
most beautiful mathematical formulas.


```{prf:algorithm} Ford–Fulkerson
:label: my-algorithm

**Inputs** Given a Network $G=(V,E)$ with flow capacity $c$, a source node $s$, and a sink node $t$

**Output** Compute a flow $f$ from $s$ to $t$ of maximum value

1. $f(u, v) \leftarrow 0$ for all edges $(u,v)$
2. While there is a path $p$ from $s$ to $t$ in $G_{f}$ such that $c_{f}(u,v)>0$
	for all edges $(u,v) \in p$:

	1. Find $c_{f}(p)= \min \{c_{f}(u,v):(u,v)\in p\}$
	2. For each edge $(u,v) \in p$

		1. $f(u,v) \leftarrow f(u,v) + c_{f}(p)$ *(Send flow along the path)*
		2. $f(u,v) \leftarrow f(u,v) - c_{f}(p)$ *(The flow might be "returned" later)*
```

```{mermaid}
graph TD;
    A-->B;
    A-->C;
    B-->D;
    C-->D;
```

| col1     | col2      |
| -------- | --------- |
| {{key2}} | {{fishy}} |


```{dropdown} Here's my dropdown
And here's my dropdown content
```

```{figure} /Images/logo.png
:name: my-fig-ref

My figure title.
```

Here is {numref}`my-fig-ref`


```{margin} An optional title
My margin content
```

````{div} full-width
```{note}
Here's a note that will take the full width
```
````

$$
  w_{t+1} = (1 + r_{t+1}) s(w_t) + y_{t+1}
$$ (my_other_label)


A link to a dollar math block: {eq}`my_other_label`
