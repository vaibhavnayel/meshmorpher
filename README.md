# Mesh Morpher
Use this repository to turn one mesh into another with the power of [NVIDIA-Kaolin](https://github.com/NVIDIAGameWorks/kaolin) and [Pytorch](pytorch.org).



## Method

We calculate the chamfer distance between 2 sampled meshes and backpropagate through it to morph a template mesh into the target. Edge length regularization is used to improve smoothness.

```markdown
optimizer = torch.optim.Adam([m1.vertices],lr=0.01)

for i in range(epochs):

    optimizer.zero_grad()
    loss=chamfer_distance(m1,m2) + edge_length(m1)
    loss.backward()
    optimizer.step()

```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/vaibhavnayel/meshmorpher/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
