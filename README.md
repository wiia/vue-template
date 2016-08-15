# vue-template
my custom template  for scaffolding Vue.js projects based on [vuejs-templates/webpack](https://github.com/vuejs-templates/webpack)

    $ vue init wiia/vue-template <project-name>


---
## css-lib
###reset.less
css reset 本身是追求`复用性`的产物，但是它自带的`全局设置`特点有时候也会带来负面影响；（当然 normalize.css 和这里不同，完全是根据另外一种原则。）
所以我把属性的 reset 设置按照`元素类型`划分，在需要使用的地方以 `mixin` 调用。

example:

    .text {
	  .re-input();
	}

###ui-utils.less
example:
	
    .line::before {
	  content: '';
	  .ui-triangle(right, 10px, 10px, 10px, #52cca3);
	}

compiles into:

    .line::before {
	  content: '';
	  display: inline-block;
	  width: 0;
	  height: 0;
	  border-style: dashed dashed dashed solid;
	  border-width: 10px 0 10px 10px;
	  border-color: transparent transparent transparent #52cca3;
	}
###variables.less
###font.less
