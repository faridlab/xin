xin
===

Xin is Single Page Application framework using javascript.

![Xin](http://xinix.co.id/storage/uploads/xin.png "SPA Framework")

# Install

```
pas install
```
[Install Pas](https://github.com/reekoheek/pas "pas - another package management and automation")

to rebuild js and css
```
gulp
```

# Watch

```
gulp watch
```

# UI

TBD

# Directive
Directives are a way to teach HTML new tricks. During DOM compilation directives are matched against the HTML and executed. This allows directives to register behavior, or transform the DOM. Could someone explain directives in AngularJS in plain English commonly used in teaching programming.

## [data-role="app"]
TBD
## [data-role="pane"]
TBD
## [data-role="view"]
The general idea is to organize your interface into logical views, backed by models, each of which can be updated independently when the model changes, without having to redraw the page. Instead of digging into a JSON object, looking up an element in the DOM, and updating the HTML by hand, you can bind your view's render function to the model's "change" event — and now everywhere that model data is displayed in the UI, it is always immediately up to date.
[Backbonejs View](http://backbonejs.org/#View "Read more backbone view concept")

__Default view__
```html
<div data-role="view" data-uri="uri" data-layout="layoutid" data-title="Title">
    ...
</div>
```

__Custom View__
```javascript
var CustomView = xin.ui.View.extend({
    events: {
        "click .icon":          "open",
        "click .button.edit":   "openEditDialog",
        "click .button.delete": "destroy"
    },
    open: function(evt) {
        // do something amazing
    },
    openEditDialog: function(evt) {
        // do something amazing
    },
    destroy: function(evt) {
        // do something amazing
    }
});
```

__HTML implementation__
```html
<div data-role="CustomView" data-uri="uri" data-layout="layoutid" data-title="Title">
    ...
</div>
```

## [data-role="layout"]
A mobile site/mobile app layout is very important to give better look. It takes considerable time to design a mobile site/mobile app layout with great look and feel.

By default xin's layout has three important parts:

1.  Header

    Used to put the title of the current page, logo and button to perform the action.

2.  Body

    Used to display main content of the page

3.  Footer

    Used to display credit and etc


![Layout](./graphics/layout.png "Layout")

```html
<div data-role="layout" data-id="default" class="xc-flex vertical">
    <div data-region="header">
        <div data-role="navbar" class="xc-flex horizontal">

            <div class="no-flex" style="left:0"></div>

            <div data-region="title" class="xin-title center">
                Simple Demo
            </div>
            <div class="no-flex" style="right:0">

            </div>
        </div>
    </div>
    <div data-region="body" class="center layout-body">

    </div>
    <div data-region="footer">
        <div class="xin-navbar">
            <div class="xin-title">
                Footer
            </div>
        </div>
    </div>
</div>

<div data-role="view" data-uri="login" data-id="login" data-layout="default" data-title="Login Title Here">
    <form action="">
        <ul data-role="list" data-model="user.model">
            <li>
                <input type="text" placeholder="Username" name="username" data-bind="name" />
            </li>
            <li>
                <input type="text" placeholder="Password" name="password" />
            </li>
        </ul>
    </form>
</div>
```

Result:
![Login](./graphics/login.png "Login")

## [data-role="drawer"]
TBD
## [data-parent-referer="your_uri"]
TBD
## [data-background="red"]
TBD
## [data-model="model"]
TBD
## [data-collection="collection"]
TBD
## [data-uri="list"]
TBD
## [data-layout="default"]
TBD
## [data-title="List"]
TBD


Directives (app, pane, view, layout, drawer, language)

# TODO

[] Fullscreen on mobile browser

#change Logs

## v0.0.*-rc
*	Theme convention using

## v0.0.1
Initial commit
