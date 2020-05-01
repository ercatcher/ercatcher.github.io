## Welcome to GitHub Pages

You can use the [editor on GitHub](https://github.com/ercatcher/ercatcher.github.io/edit/master/README.md) to maintain and preview the content for $\alpha$  your website in Markdown files.

Whenever you commit to this 
$$\frac{1}{2}$$
 {% raw %}
  $$a^2 + b^2 = c^2$$ --> note that all equations between these tags will not need escaping! 
 {% endraw %}
repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

Happens-Before ($HB$) is a strict partially ordered set on nodes $N$ which is the set of $e.s$, $e.e$, and $e.i$ for all $e \in E$. The $HB$ relation is defined as:
$$n_1 \prec n_2 \iff (H(n_2) \Rightarrow H(n_1) \land HBD(n_1, n_2)$$
where $H(n_1)$ means the node $n_1$ is executed (or happens) and $HBD(n_1, n_2)$ means the node $n_1$ happens before node $n_2$ in all possible orders of execution in run time. 


Let say $HB^{*}(E)$ is the complete and sound happens-before ordered set on events $E$: it has all the correct happens-before relations and no single one of the relations are incorrect. If an app is executed in real world, two events with a correct happens-before relation always will be executed in that order. $HB^{*}$ satisfies the properties below (we prove the correctness of these properties in the appendix).
\begin{itemize}
    \item \textit{Irreflexivity}
    $$ \forall n \in N: n \prec n$$
    \item \textit{Transitivity}:
    $$\forall n, n', n'' \in N : n \prec n' \land n' \prec n'' \Rightarrow n \prec n''$$
    \item \textit{Asymmetry}:
    $$\nexists n, n' \in N:  n \prec n' \land n' \prec n$$
    \item Intra-Event Order:
    $$\forall e \in E(t) : e_i \prec e_s \land e_s \prec e_n \land$$
    $$\forall n \in e.B: e.s \prec n \land n \prec e.e \land (\forall n' \in SUCC(n): n \prec n')$$
    \item Event Atomicty:
    $$\nexists e, e' \in E(t): (e'.s \prec e.e \land e'.s \nprec e.s) \lor (e'.e \prec e.e \land e'.e \nprec e.s) $$
    \item Same Event Queue Order:
    $$t \in M \Rightarrow \forall e, e' \in E(t): e.i \prec e'.i \land e.d \prec e'.d \Rightarrow e.e \prec e'.s$$
\end{itemize}




```markdown
Syntax highlighted code block

# Header 1
## Header 2


### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/ercatcher/ercatcher.github.io/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
