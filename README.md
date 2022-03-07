## Welcome to GitHub Pages

You can use the [editor on GitHub](https://github.com/dawals/dawals.github.io/edit/main/README.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown
import matplotlib.pyplot as plt 
import numpy as np
 
plt.figure(figsize=(16,16))
fig = plt.figure(1)
ax = fig.add_subplot(111) 
 
# set up axis 
# Move left y-axis and bottom x-axis to zero
ax.spines['left'].set_position('zero')
ax.spines['bottom'].set_position('zero') 
# Eliminate upper and right axes
ax.spines['right'].set_color('none') 
ax.spines['top'].set_color('none') 
# Show ticks in the left and lower axes only
ax.xaxis.set_ticks_position('bottom') 
ax.yaxis.set_ticks_position('left')
 
x = np.linspace(-12, 12, 500)
y1 = (1/x**2) -5
# x, y
ax.plot(x, y1,linewidth=2.5,color='steelblue',linestyle='-')
# Asymptote
ax.axvline(x=-0.12,color='firebrick',linestyle='-',linewidth=2.5)
ax.axvline(x=0.12,color='firebrick',linestyle='-',linewidth=2.5)
ax.axhline(y=-5.43,color='firebrick',linestyle='-',linewidth=2.5)
 
plt.title(r"$f(x) = \frac{1}{x^2} -5 $"+"\n", fontsize=20)
 
ax.set_xticks(np.arange(-10,10,1))
ax.set_yticks(np.arange(-10,10,1))
 
ax.set_xbound(-10,10)
ax.set_ybound(-10,10) 
 
plt.savefig('asymptotes02.png', bbox_inches='tight')
plt.show()

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

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

For more details see [Basic writing and formatting syntax](https://docs.github.com/en/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/dawals/dawals.github.io/settings/pages). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.
