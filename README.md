# Coding Recommandations

This readme describes the coding recommandations for the whole
organisation. All repositories within this organisation should follow
those rules.

## Programming Languages
### general
  - write testable code
  - classes and functions should not rely on getting there information
    by them self. e.g. the constructor should not collect the
    necessary information by reading from file or from global values.
    values should be given by constructors parameter or set by setters.
  - follow project coding standard
  - follow clean code principals
  - write comments to explain code which seams not usual or as you
    write you know it will confuse other persons or yourself
  - comments and variable values have to be written in english!
  - files should have newlines at the end of the file

### php

### javascript

### typescript

### python
   - follow invenio coding guides, which should be more ore less the
     pep rules!
   - follow pep rules
   - use black as the default formater
   - use where ever possible TypedDict's or dataclass. if there is a
     return value in the form {"key": "value"} then it should be
     modeled as a TypedDict. If the "json" has to much of key->value
     pairs, then it should be class with the object as a property.
     there it is ok not to create a type for it. e.g. marc21!

## html
  - follow project coding standard
  - only lowercase element names
  - avoid elements for layout porpose only
  - use html5 elements like section or article
  - don't use html elements for styling, use css instead
  - encapsulate views like records with a element (e.g. div)

## commits
  - after the commit it should still work
    - check tests before commit!
  - single responsibility
    - if there is a "and" in the head then it should be more then one
      commit
    - don't mix refactoring with new functionalities
    - to be clear: it is highly possible that a commit has in the diff
      only one line changed and the commit message has multiple
      paragraphs to explain why this change happened
  - expressive commit messages
    - explain why changes happend
    - explain how things are done
    - explain what was wrong
    - reference design decisions
  - less than 80 characters
  - head + body separated by white line

## merge
  - create personal repository on github and create for every change
    on the main repository a pull request
  - which has to be reviewed

## workflows
### make changes
  - create a issue on the original repository
  - implement that specific issue on your personal repository
  - create a pull request with reference to that issue and a short
    description what has been done in this pull request
  - loop isPositiveReviewed
    - the person which is responsible for the repository should review
      the pull request
    - apply possible change suggestions
    - add possible changes
  - the responsible person of the repository merges the pull request
    and closes the issue. This person uses the pull request
    description to add it to the merge description.
