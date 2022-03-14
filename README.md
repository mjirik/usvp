# usvp


```bash
conda create -n jupyterslides -c conda-forge python=3.9 scikit-learn scikit-image jupyterlab jupyterlab_vim nbconvert=6.1 nodejs
```



# Build the slides

See the tutorial [Present Your Data Science](https://medium.com/learning-machine-learning/present-your-data-science-projects-with-jupyter-slides-75f20735eb0f)

```shell
git submodule add https://github.com/hakimel/reveal.js.git reveal.js
```

```shell
jupyter-nbconvert --to slides slides/Tasks_in_Computer_Vision.ipynb --reveal-prefix=../reveal.js 
```

```shell
jupyter-nbconvert --to slides slides/Tasks_in_Computer_Vision.ipynb --reveal-prefix=../reveal.js --SlidesExporter.reveal_theme="sky"
```


```shell
jupyter nbconvert --to slides slides/Tasks_in_Computer_Vision.ipynb --reveal-prefix=../reveal.js --SlidesExporter.reveal_scroll=True --SlidesExporter.reveal_theme="sky" --SlidesExporter.reveal_header="<H1>cat.jpg</H1>"
```

