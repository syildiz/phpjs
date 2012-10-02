---
layout: page
title: "JavaScript is_object function"
comments: true
sharing: true
footer: true
alias:
- /functions/is_object:450
- /functions/450
---
A JavaScript equivalent of PHP's is_object

{% codeblock var/is_object.js lang:js https://raw.github.com/kvz/phpjs/master/functions/var/is_object.js raw on github %}
function is_object (mixed_var) {
    // http://kevin.vanzonneveld.net
    // +   original by: Kevin van Zonneveld (http://kevin.vanzonneveld.net)
    // +   improved by: Legaev Andrey
    // +   improved by: Michael White (http://getsprink.com)
    // *     example 1: is_object('23');
    // *     returns 1: false
    // *     example 2: is_object({foo: 'bar'});
    // *     returns 2: true
    // *     example 3: is_object(null);
    // *     returns 3: false
    if (Object.prototype.toString.call(mixed_var) === '[object Array]') {
        return false;
    }
    return mixed_var !== null && typeof mixed_var == 'object';
}
{% endcodeblock %}

 - [view on github](https://github.com/kvz/phpjs/blob/master/functions/var/is_object.js)
 - [edit on github](https://github.com/kvz/phpjs/edit/master/functions/var/is_object.js)