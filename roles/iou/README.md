# IOU role

IOU stands for IOS on Unix. This role prepares environment for IOU. As a matter of fact it builds a docker container.
It uses some binaries from [iou-web repo](#https://github.com/dainok/iou-web).

> Playbook does not install IOU images.

This role is kind of abstract. It is created for other roles could depend on it.

You may use it to create your own topology. All you need is:
- put IOU images for l2 and l3 devices inside `files` directory in your role.
- populate `vars/images.yml` with their names:
```
images:
  l2: "l2_image_filename"
  l3: "l3_image_filename"
```
- create `instances` var in your `vars/main.yml`. Take a look at `defaults/main.yml` of this role to get an idea how it should look like.
- create `NETMAP` file and put it inside `files` directory of your role.
