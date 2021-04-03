---
title: An analogy for containers
published: true
tags: technical
---

I've always struggled to keep my Docker and container terminology straight. I don't work with it frequently enough to maintain a working knowledge, yet I encounter it often enough that I should know it better than I do. My problem is the naming is too similar and the metaphors are mixed. Container vs container image for example -- similar names, one leverages the metaphor of a physical shipping container while the other borrows the "image" terminology from the VM space.

If you've never had an issue remembering any of this, great! However, if you share my pains, I hope the following analogy helps you learn and retain the difference between the various container and Docker concepts.

Here's the tl;dr:

| Container concept | Cooking metaphor |
| :------------------ | :----------------- |
| Dockerfile | Recipe |
| docker build | Following the recipe |
| Container image | Completed dish |
| Layer | Replaceable part of dish |
| Container | Dish served on a table |
| Image repository | Grocery store |
| docker compose | Serving several dishes together |


# A Dockerfile is your recipe
Ok, I know this isn't original -- almost every explanation of Docker and containers uses this metaphor. But it's a good one. I'm surprised I've never seen it extended through the rest of Docker's concepts. The recipe metaphor can go a little deeper too -- your typical recipe describes both specific ingredients and step-by-step instructions on how to combine those ingredients. This is true of a Dockerfile as well -- you describe the resources you need and what to do with them.

### Docker build is following your recipe
If we stick with the cooking analogy, Docker build is the act of grabbing your ingredients from the fridge and pantry, prepping them, and combining them -- all according to your recipe. The result…

### A container image is your finished dish
After you successfully follow the recipe, you get a result: your completed dish. It consumed ingredients and is now taking up space in your kitchen. This is just like a container image -- its resources like another image, an npm library, your source code, etc… all put together in a particular way and taking up space. But just like no one is immediately eating from your dish in whatever pot or pan you've cooked it in, no one is directly using the container image. It still needs to be put into a usable, consumable state.

Another twist on this is when you're cooking, say, a pasta dish, you could create your pasta from scratch. Or you could use pre-made pasta. A similar idea exists with container images -- you could create one from scratch or you can start from a pre-made one that already has many of the resources you need downloaded and configured.

### A container is your dish served on a plate with utensils
The last step before someone can enjoy your dish is for the food to be served. It needs to be prepared and served in a way that someone can eat it. This is kind of like the relation between a container image and a container instance. The container instance can be used and interacted with. It's the deliverable. And just like a dish that's served uses up limited plates, utensils, and space on your table, your container is now consuming limited resources on your server like ports and memory.

# Abusing the metaphor
I hope this metaphor is clicking with you so far. If so, let's keep going with it to explain a few more important Docker concepts.

### An image repository is your grocery store
Early I described how your container image is a finished dish sitting in your kitchen and you can leverage other images to create yours much like you can pull pre-made parts of your dish from your pantry. However, much like your pantry and fridge, your computer has limited space. It doesn't make sense for it to hold a lot of images. In the real world we solve this by having grocery stores we can go to just before making a dish. In the container world, there's image repositories. 

### A layer is part of your dish you can swap out
Imagine you've handmade a bunch of pasta, combined it with a homemade marinara sauce, and served the final dish. But the next night you want something a little different, so you make a homemade white sauce instead. You can take this sauce and combine it with the handmade pasta from the previous night. It goes without saying that it would be ridiculous to throw out the perfectly good pasta from the night before and make more from scratch. That's the idea behind layers in a container image -- don't download every resource, run every compilation, move every file, etc… if you don't have to. 

### Docker compose is serving a meal with several dishes
If you think about the last time you went to a restaurant and recall how everything came out in a precise order -- appetizers came out for first and the entrees came out all at the same time. In the back of the restaurant, not only are they putting together dishes according to recipes, but they're orchestrating when to execute those recipes to get multiple dishes to the right table at the right time. This is the idea behind docker compose -- organizing multiple containers to work together. 