# `craft.users()`

You can access your site’s users from your templates with `craft.users()`. It returns a new [element query](../../element-queries.md) of type <api:craft\elements\db\UserQuery>.

Elements returned by [all()](api:craft\elements\db\ElementQuery::all()), [one()](api:craft\elements\db\ElementQuery::one()), etc., will be of type <api:craft\elements\User>.

```twig
{% set authors = craft.users()
    .group('authors')
    .all() %}

<ul>
    {% for author in authors %}
        <li><a href="{{ url('authors/'~author.id) }}">{{ author.name }}</a></li>
    {% endfor %}
</ul>
```

<!-- BEGIN PARAMS -->

### `inReverse`

Whether the results should be queried in reverse.


[Reference](api:craft\elements\db\ElementQuery::$inReverse)

### `asArray`

Whether to return each element as an array. If false (default), an object
of [$elementType](https://docs.craftcms.com/api/v3/craft-elements-db-elementquery#property-$elementtype) will be created to represent each element.


[Reference](api:craft\elements\db\ElementQuery::$asArray)

### `id`

The element ID(s). Prefix IDs with "not " to exclude them.


[Reference](api:craft\elements\db\ElementQuery::$id)

### `uid`

The element UID(s). Prefix UIDs with "not " to exclude them.


[Reference](api:craft\elements\db\ElementQuery::$uid)

### `fixedOrder`

Whether results should be returned in the order specified by [id()](https://docs.craftcms.com/api/v3/craft-elements-db-elementquery#method-id).


[Reference](api:craft\elements\db\ElementQuery::$fixedOrder)

### `status`

The status(es) that the resulting elements must have.


[Reference](api:craft\elements\db\ElementQuery::$status)

### `archived`

Whether to return only archived elements.


[Reference](api:craft\elements\db\ElementQuery::$archived)

### `dateCreated`

When the resulting elements must have been created.


[Reference](api:craft\elements\db\ElementQuery::$dateCreated)

### `dateUpdated`

When the resulting elements must have been last updated.


[Reference](api:craft\elements\db\ElementQuery::$dateUpdated)

### `siteId`

The site ID that the elements should be returned in.


[Reference](api:craft\elements\db\ElementQuery::$siteId)

### `enabledForSite`

Whether the elements must be enabled for the chosen site.


[Reference](api:craft\elements\db\ElementQuery::$enabledForSite)

### `relatedTo`

The element relation criteria.


[Reference](api:craft\elements\db\ElementQuery::$relatedTo)

### `title`

The title that resulting elements must have.


[Reference](api:craft\elements\db\ElementQuery::$title)

### `slug`

The slug that resulting elements must have.


[Reference](api:craft\elements\db\ElementQuery::$slug)

### `uri`

The URI that the resulting element must have.


[Reference](api:craft\elements\db\ElementQuery::$uri)

### `search`

The search term to filter the resulting elements by.


[Reference](api:craft\elements\db\ElementQuery::$search)

### `ref`

The reference code(s) used to identify the element(s).

This property is set when accessing elements via their reference tags, e.g. {entry:section/slug}.


[Reference](api:craft\elements\db\ElementQuery::$ref)

### `with`

The eager-loading declaration


[Reference](api:craft\elements\db\ElementQuery::$with)

### `admin`

Whether to only return users that are admins.


[Reference](api:craft\elements\db\UserQuery::$admin)

### `can`

The permission that the resulting users must have.


[Reference](api:craft\elements\db\UserQuery::$can)

### `groupId`

The tag group ID(s) that the resulting users must be in.


[Reference](api:craft\elements\db\UserQuery::$groupId)

### `email`

The email address that the resulting users must have.


[Reference](api:craft\elements\db\UserQuery::$email)

### `username`

The username that the resulting users must have.


[Reference](api:craft\elements\db\UserQuery::$username)

### `firstName`

The first name that the resulting users must have.


[Reference](api:craft\elements\db\UserQuery::$firstName)

### `lastName`

The last name that the resulting users must have.


[Reference](api:craft\elements\db\UserQuery::$lastName)

### `lastLoginDate`

The date that the resulting users must have last logged in.


[Reference](api:craft\elements\db\UserQuery::$lastLoginDate)


<!-- END PARAMS -->
