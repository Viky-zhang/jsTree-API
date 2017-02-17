# jsTree 核心功能（core functionality）

## $.jstree
包含所有 jstree 相关的函数和变量，包括用于创建、访问、维护实例的类和方法。


## $.jstree.version
jstree 的版本号


## $.jstree.defaults
包含用于创建新实例的默认配置


## $.jstree.defaults.plugins
默认是`[]`。

配置实例中使用的插件。是一个字符串数组，每个字符串是一个插件名。


## $.jstree.plugins
存放所有已加载的插件（内部用）


## $.jstree.create (el [, options])
创建一个 jstree 实例

| 参数/返回 |   描述   |
| --------   | -----  |
| `el`       | `DOMElement` `jQuery` `String`，要创建实例的元素，可以是 jQuery 对象或一个选择器 |
| `options`  | `Object` 此实例的配置（扩展自`$.jstree.defaults`）  |
| `返回`      | `jsTree` 新的实例    |


## $.jstree.destroy ()
从 DOM 中删除 jstree 的所有痕迹，并销毁所有的实例。


## $.jstree.core (id) - -  `private`
jstree 类的构造函数，仅用于内部。

| 参数 |   描述   |
| --------   | -----  |
| `id`       | `Number` 此实例的索引号（index） |


$.jstree.reference (needle)
获取一个已存在实例的引用。

| 参数/返回 |   描述   |
| --------   | -----  |
| `needle`   | `DOMElement` `jQuery` `String` |
| `返回`      | `jsTree` `null` 实例，如果找不到实例则返回 `null` |

**Examples**
```js
// provided a container with an ID of "tree", and a nested node with an ID of "branch"
// all of there will return the same instance
$.jstree.reference('tree');
$.jstree.reference('#tree');
$.jstree.reference($('#tree'));
$.jstree.reference(document.getElementByID('tree'));
$.jstree.reference('branch');
$.jstree.reference('#branch');
$.jstree.reference($('#branch'));
$.jstree.reference(document.getElementByID('branch'));
```


## $().jstree([arg])

## $(':jstree')

## $.jstree.defaults.core

## $.jstree.defaults.core.data

## $.jstree.defaults.core.strings

## $.jstree.defaults.core.check_callback

## $.jstree.defaults.core.error

## $.jstree.defaults.core.animation

## $.jstree.defaults.core.multiple

## $.jstree.defaults.core.themes

## $.jstree.defaults.core.themes.name

## $.jstree.defaults.core.themes.url

## $.jstree.defaults.core.themes.dir

## $.jstree.defaults.core.themes.dots

## $.jstree.defaults.core.themes.icons

## $.jstree.defaults.core.themes.ellipsis

## $.jstree.defaults.core.themes.stripes

## $.jstree.defaults.core.themes.variant

## $.jstree.defaults.core.themes.responsive

## $.jstree.defaults.core.expand_selected_onload

## $.jstree.defaults.core.worker

## $.jstree.defaults.core.force_text

## $.jstree.defaults.core.dblclick_toggle

## plugin (deco [, opts]) - -  `private`



## init (el, optons) - -  `private`



## init.jstree Event



## loading.jstree Event



## destroy ()



## Create prototype node



## teardown () - -  `private`



## bind () - -  `private`



## loaded.jstree Event



## ready.jstree Event



## unbind () - -  `private`



## trigger (ev [, data]) - -  `private`



## get_container ()



## get_container_ul () - -  `private`



## get_string (key) - -  `private`



## _firstChild (dom) - -  `private`



## _nextSibling (dom) - -  `private`



## _previousSibling (dom) - -  `private`



## get_node (obj [, as_dom])



## get_path (obj [, glue, ids])



## get_next_dom (obj [, strict])



## get_prev_dom (obj [, strict])



## get_parent (obj)



## get_children_dom (obj)



## is_parent (obj)



## is_loaded (obj)



## is_loading (obj)



## is_open (obj)



## is_closed (obj)



## is_leaf (obj)



## load_node (obj [, callback])



## load_node.jstree Event



## _load_nodes (nodes [, callback]) - -  `private`



## load_all ([obj, callback])



## load_all.jstree Event



## _load_node (obj [, callback]) - -  `private`



## _node_changed (obj [, callback]) - -  `private`



## _append_html_data (obj, data) - -  `private`



## model.jstree Event



## _append_json_data (obj, data) - -  `private`



## _parse_model_from_html (d [, p, ps]) - -  `private`



## _parse_model_from_flat_json (d [, p, ps]) - -  `private`



## _parse_model_from_json (d [, p, ps]) - -  `private`



## _redraw () - -  `private`



## redraw.jstree Event



## redraw ([full])



## draw_children (node) - -  `private`



## redraw_node (node, deep, is_callback, force_render) - -  `private`



## open_node (obj [, callback, animation])



## before_open.jstree Event



## open_node.jstree Event



## after_open.jstree Event



## _open_to (obj) - -  `private`



## close_node (obj [, animation])



## close_node.jstree Event



## after_close.jstree Event



## toggle_node (obj)



## open_all ([obj, animation, original_obj])



## open_all.jstree Event



## close_all ([obj, animation])



## close_all.jstree Event



## is_disabled (obj)



## enable_node (obj)



## enable_node.jstree Event



## disable_node (obj)



## disable_node.jstree Event



## is_hidden (obj)



## hide_node (obj)



## hide_node.jstree Event



## show_node (obj)



## show_node.jstree Event



## hide_all ()



## hide_all.jstree Event



## show_all ()



## show_all.jstree Event



## activate_node (obj, e) - -  `private`



## activate_node.jstree Event



## hover_node (obj) - -  `private`



## hover_node.jstree Event



## dehover_node (obj) - -  `private`



## dehover_node.jstree Event



## select_node (obj [, supress_event, prevent_open])



## select_node.jstree Event



## changed.jstree Event



## deselect_node (obj [, supress_event])



## deselect_node.jstree Event



## select_all ([supress_event])



## select_all.jstree Event



## deselect_all ([supress_event])



## deselect_all.jstree Event



## is_selected (obj)



## get_selected ([full])



## get_top_selected ([full])



## get_bottom_selected ([full])



## get_state () - -  `private`



## set_state (state [, callback]) - -  `private`



## set_state.jstree Event



## refresh ()



## refresh.jstree Event



## refresh_node (obj)



## refresh_node.jstree Event



## set_id (obj, id)



## set_id.jstree Event



## get_text (obj)



## set_text (obj, val) - -  `private`



## set_text.jstree Event



## get_json ([obj, options])



## create_node ([par, node, pos, callback, is_loaded])



## create_node.jstree Event



## rename_node (obj, val)



## rename_node.jstree Event



## delete_node (obj)



## delete_node.jstree Event



## check (chk, obj, par, pos) - -  `private`



## last_error ()



## move_node (obj, par [, pos, callback, is_loaded])



## move_node.jstree Event



## copy_node (obj, par [, pos, callback, is_loaded])



## copy_node.jstree Event



## cut (obj)



## cut.jstree Event



## copy (obj)



## copy.jstree Event



## get_buffer ()



## can_paste ()



## paste (obj [, pos])



## paste.jstree Event



## clear_buffer ()



## clear_buffer.jstree Event



## edit (obj [, default_text, callback])



## set_theme (theme_name [, theme_url])



## set_theme.jstree Event



## get_theme ()



## set_theme_variant (variant_name)



## get_theme ()



## show_stripes ()



## show_stripes.jstree Event



## hide_stripes ()



## hide_stripes.jstree Event



## toggle_stripes ()



## show_dots ()



## show_dots.jstree Event



## hide_dots ()



## hide_dots.jstree Event



## toggle_dots ()



## show_icons ()



## show_icons.jstree Event



## hide_icons ()



## hide_icons.jstree Event



## toggle_icons ()



## show_icons ()



## show_ellipsis.jstree Event



## hide_ellipsis ()



## hide_ellipsis.jstree Event



## toggle_icons ()



## set_icon (obj, icon)



## get_icon (obj)



## hide_icon (obj)



## show_icon (obj)