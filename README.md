[![Published on webcomponents.org](https://img.shields.io/badge/webcomponents.org-published-blue.svg?style=flat-square)](https://www.webcomponents.org/element/GeoloeG/iron-pullable-container)

# `<iron-pullable-container>`

## Descripton

`<iron-pullable-container>` enable a given container to be pulled and be notified if a certain threshold has been reached to take any actions, like refreshing the container's content.

## Install

Install the component using [Bower](http://bower.io/):

```sh
$ bower install iron-pullable-container --save
```

## Usage

Import Custom Element:

```html
<link rel="import" href="bower_components/iron-pullable-container/iron-pullable-container.html">
```

And then use it:

```html
    <iron-pullable-container 
      on-iron-pull-start="_handlePullStart"
      on-iron-pull-end="_handlePullEnd"
      auto-close>
      <span id="spanId" class="underlay">Loading...</span>
      <div class="container">
        <div class="big">Pull me down!</div>
        <div class="extend">(I was pulled [[_nbPull]] time(s))</div>
      </div>
    </iron-pullable-container>
 
    ...

    scope._handlePullStart = function() {
      scope._nbPull++;
      scope.$.spanId.style.opacity = 1;
    };

    scope._handlePullEnd = function() {
      scope.$.spanId.style.opacity = 0;
    };
```

See the [Documentation](https://geoloeg.github.io/iron-pullable-container/) for more options.

## More Demos

[https://geoloeg.github.io/iron-pullable-container/](https://geoloeg.github.io/iron-pullable-container/components/iron-pullable-container/demo/)

## Discussing

If you have any questions, you can find me on the [Polymer Slack Channel](https://polymer.slack.com/), or just raise an Issue.

## Contributing

1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -m 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request :D
