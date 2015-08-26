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
| ulClass| Class name of ul | `'related-posts'` |
| liClass| Class name of li | `'related-posts-item'` |
| orderBy| `'date'` or `'random'`<br> When the number of matched tags is the same, list is ordered by date or random. | `'date'` |
| isAscending| Ascending or descending when list is ordered by date. | `false`

### Examples

```html
<%- list_related_posts({maxCount: 10, orderBy: 'random'}) %>
```
