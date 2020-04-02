# useful-js-lib

## Vue
- [vuex Pathify](https://davestewart.github.io/vuex-pathify/#/)

## Utility
- [jquery.nodoubletapzoom.js](https://gist.github.com/randomm/4955933)
- [hotkey](https://github.com/jaywcjlove/hotkeys)
- [Background Video (parallax supported)](https://github.com/linnett/backgroundVideo)

## Form
- [formvalidation](https://formvalidation.io/)

## Custom Event

```
<script>
    // CustomEvent micro-polyfill for Internet Explorer
    (function() {
        if (typeof window.CustomEvent === "function") {
            return false;
        }

        function CustomEvent(event, params) {
            params = params || { bubbles: false, cancelable: false, detail: undefined };
            var evt = document.createEvent("CustomEvent");
            evt.initCustomEvent(event, params.bubbles, params.cancelable, params.detail);
            return evt;
        }

        CustomEvent.prototype = window.Event.prototype;
        window.CustomEvent = CustomEvent;
    })();
</script>
```
