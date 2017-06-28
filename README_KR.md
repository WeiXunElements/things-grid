# Dataludi로 Elidom Framework에 필요한 grid들을 구현한 Grid Set

# things-resource-grid
## 기본 리소스 그리드로서 Pagination을 지원하고 import, export, add, delete, save가 가능한 그리드, Things.ResourceGridBehavior에 필요한 모든 구현이 포함되어 있다.

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

Element dependencies are managed via [Bower](http://bower.io/). You can
install that via:

    npm install -g bower

Then, go ahead and download the element's dependencies:

    bower install


## Playing With Your Element

If you wish to work on your element in isolation, we recommend that you use
[Polyserve](https://github.com/PolymerLabs/polyserve) to keep your element's
bower dependencies in line. You can install it via:

    npm install -g polyserve

And you can run it via:

    polyserve
