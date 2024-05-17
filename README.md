

# usvp


[Experiment evaluation in Computer Vision](https://mjirik.github.io/usvp/slides/experiment_evaluation_in_computer_vision.slides.html)

[Data is all you need](https://mjirik.github.io/usvp/slides/data_is_all_you_need.slides.html)


[Javorna 2024](https://mjirik.github.io/usvp/slides/2024-05-Javorna.slides.html)

# Build the slides

https://sophiamyang.github.io/slides_github_pages/


## Create environment

```bash


conda create -n jupyterslides2 -c conda-forge python=3.12 scikit-learn scikit-image jupyterlab jupyterlab_vim nbconvert nodejs jupyterlab_rise
```

or older setup
```bash
conda create -n jupyterslides -c conda-forge python=3.9 scikit-learn scikit-image jupyterlab jupyterlab_vim nbconvert=6.1 nodejs
```


## Build the slides

See the tutorial [Present Your Data Science](https://medium.com/learning-machine-learning/present-your-data-science-projects-with-jupyter-slides-75f20735eb0f)

```shell
git submodule add https://github.com/hakimel/reveal.js.git reveal.js
```

```shell
jupyter-nbconvert.exe --to slides --reveal-prefix=../reveal.js --SlidesExporter.reveal_config=custom_reveal_config.js --SlidesExporter.reveal_theme="white" --SlidesExporter.reveal_scroll=True .\slides\2024-05-Javorna.ipynb

jupyter-nbconvert --to slides slides/experiment_evaluation_in_computer_vision.ipynb --reveal-prefix=../reveal.js 
jupyter-nbconvert --to slides slides/data_is_all_you_need.ipynb --reveal-prefix=../reveal.js 
```

```shell
jupyter-nbconvert --to slides slides/Tasks_in_Computer_Vision.ipynb --reveal-prefix=../reveal.js --SlidesExporter.reveal_theme="sky"
```


```shell
jupyter nbconvert --to slides slides/Tasks_in_Computer_Vision.ipynb --reveal-prefix=../reveal.js --SlidesExporter.reveal_scroll=True --SlidesExporter.reveal_theme="sky" --SlidesExporter.reveal_header="<H1>cat.jpg</H1>"
```

jupyter-nbconvert --to latex slides\data_is_all_you_need.ipynb --reveal-prefix=../reveal.js

Parameters can be controlled by GET parameters of URL:

```
file:///C:/Users/Jirik/projects/usvp/slides/2024-05-Javorna.slides.html?embedded=false&width=1600&height=1200&margin=0.04&minScale=0.4&maxScale=1.0#/7
```

## Push to github


```shell
git push
```

