# usvp


```bash
conda create -n jupyter-slides -c conda-forge python jupyter pandoc scikit-learn scikit-image jupyter_contrib_nbextensions jupyterlab jupyterlab_vim
```



# Build the slides

See the tutorial [Present Your Data Science](https://medium.com/learning-machine-learning/present-your-data-science-projects-with-jupyter-slides-75f20735eb0f)

```shell
git submodule add https://github.com/hakimel/reveal.js.git reveal.js
```

```shell
jupyter nbconvert --to slides index.ipynb --reveal-prefix=reveal.js 
```

```shell
jupyter nbconvert --to slides index.ipynb --reveal-prefix=reveal.js --SlidesExporter.reveal_theme=serif  --SlidesExporter.reveal_scroll=True  --SlidesExporter.reveal_transition=none