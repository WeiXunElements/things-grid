# This is a Grid Set that implements grids needed for Elidom Framework with DataLudi.

# things-resource-grid
## A grid that supports Pagination and can import, export, add, delete, and save as a basic resource grid. It contains all necessary implementations of Things.ResourceGridBehavior.

  Example:
```html
    <things-ajax
      auto
      resource-url="diy_services/ElidomGridModel/query.json"
      method="GET"
      last-response="{{gridModel}}">
    </things-ajax>

    <things-ajax
      auto
      resource-url="diy_services/ElidomGridColumn/query.json"
      method="GET"
      last-response="{{gridColumns}}">
    </things-ajax>

    <things-ajax
      id="search-resource"
      resource-url="terminologies"
      resource-action="index"
      last-response="{{gridData}}">
    </things-ajax>

    <things-resource-grid
      id="grid"
      model="[[gridModel]]"
      columns="[[gridColumns]]"
      data="[[gridData.items]]"
      total-count="[[gridData.total]]"
      current-page="1"
      limit="50"
      grid-save-action="terminologies/update_multiple">
    </things-resource-grid>
```

## Dependencies

Element dependencies are managed via [Bower](http://bower.io/). You can install that via:

    npm install -g bower

Then, go ahead and download the element's dependencies:

    bower install

## Playing With Your Element

If you wish to work on your element in isolation, we recommend that you use
[Polyserve](https://github.com/PolymerLabs/polyserve) to keep your element's
bower dependencies in line. You can install it via:

    npm install -g polymer-cli

And you can run it via:

    polymer serve

Once running, you can preview your element at
`http://localhost:8080/components/things-grid/`, where `things-grid` is the name of the directory containing it.
