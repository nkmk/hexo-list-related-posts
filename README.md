# hexo-list-related-posts

A hexo plugin that generates a list of links to related posts based on tags.

List is ordered by the number of matched tags.

## Install

```sh
$ npm install hexo-list-related-posts --save
```

## Usage

Add `<%- list_related_posts([options]) %>` in template file for article.

## Options
| option | description | default |
| :--- | :--- | :--- |
| maxCount| Maximum count of a list | `5` |
| pClass| Class name of p when there is no related post | `'related-posts-none'` |
| ulClass| Class name of ul | `'related-posts'` |
| liClass| Class name of li | `'related-posts-item'` |
| aClass| Class name of a | `'related-posts-link'` |
| generateAbstract| Generate abstract or not | `false` |
| abstractClass| Class name of abstract of content | `'related-posts-item-abstract'` |
| abstractLength| Length of abstract | `110` |
| orderBy| `'date'` or `'random'`<br> When the number of matched tags is the same, list is ordered by date or random. | `'date'` |
| isAscending| Ascending or descending when list is ordered by date. | `false`

### Examples

```html
<%- list_related_posts({maxCount: 10, orderBy: 'random'}) %>
```

To generate abstract of content
```html
<%- list_related_posts({maxCount: 10, orderBy: 'random', generateAbstract: true}) %>
```

#### Abstract of content CSS
```
.related-posts-item-abstract {
  overflow: hidden;
  white-space: nowrap;
  text-overflow: ellipsis;  /* ends with '...' of abstract */
}
```
