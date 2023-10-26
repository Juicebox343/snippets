# snippets
Collection of commonly used lines of code, might save a minute or two of searching.

## CSS

Reserve hover states for devices that support hover. 
Prevents sticky hover state sometimes encountered on mobile.

```
.cool-html-element{
  background-color: var(--wp--preset--color--light-blue);
  @media (hover: hover) {
    &:hover{ 
      background-color: var(--wp--preset--color--navy);
    }
  }
}
```

### WordPress

Reference color defined in theme.json.
```
var(--wp--preset--color--blue);
```

Reference spacing defined in theme.json
```
var(--wp--preset--spacing--80-40);
```

Reference content widths defined in theme.json
```
var(--wp--style--global--wide-size);
```
```
var(--wp--style--global--content-size);
```

## JS

## PHP

## TOOLS

### Git

Commited changes to the wrong branch, want to undo commit but retain changes so you can apply them elsewhere

```
git reset --soft HEAD^
```

### Docker
### Lando

Create new user for WordPress site using Lando and the WP-CLI

```
lando wp user create name email@email.com --role=administrator --url=mylocal.site
```

### Terminus

Create new user on a pantheon environment using Terminus and the WP-CLI

```
terminus wp pantheon-project.environment-name -- user create username email@email.com --role=administrator --user_pass="setAPassword"
```

### WP-CLI

Search all WordPress tables and replace something with something else. - Could be optimized I'm sure.
```
wp search-replace 'replace-me' 'with-me' --precise --recurse-objects --all-tables
```
