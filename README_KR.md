# 이는 DataLudi로 Elidom Framework에 필요한 grid들을 구현한 Grid Set이다.

# things-resource-grid
## 기본 리소스 그리드로서, Pagination을 지원하고 import, export, add, delete, save가 가능한 그리드. 여기에는 Things.ResourceGridBehavior에 필요한 모든 구현이 포함되어 있다.

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

element의 종속성은 [Bower](http://bower.io/)를 통해 관리되며, 아래의 방법을 통해 설치할 수 있다.

    npm install -g bower

다음, element의 종속성을 다운로드한다.

    bower install

## Playing With Your Element

element를 독립적으로 처리하려면 [Polyserve](https://github.com/PolymerLabs/polyserve)를 사용하여 element의 bower 의존성을 유지하도록 하며, 이는 아래의 방법을 통해 설치할 수 있다.

    npm install -g polymer-cli

그리고, 아래의 방법을 통해 실행할 수 있다.

    polymer serve

element를 실행한 경우, `things-grid`가 디렉토리 이름으로 포함되어 있는 `http://localhost:8080/components/things-grid/`를 통해 이를 미리 확인할 수 있다.
