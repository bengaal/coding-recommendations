# Coding Recommandations

This readme describes the coding recommandations for the whole
organisation. All repositories within this organisation should follow
these rules.

## Programming Languages
### General
  - Write testable code.
  - Classes and functions should not rely on getting their information
    by themselves. E.g. the constructor should not collect the
    necessary information by reading from file or from global values.
    Values should be given by constructors parameter or set by setters.
  - Follow project coding standard.
  - Follow clean code principals.
  - Write comments to explain code which seems unusual or as you
    write you know it will lead to confusion.
  - Comments and variable values have to be written in English.
  - Files should have newlines at the end of the file.

### PHP

### JavaScript

### TypeScript

### Python
   - Follow invenio coding guides, which should be more or less the
     pep rules!
   - Follow pep rules.
   - Use black as the default formatter.
   - Use wherever possible TypedDict's or dataclass. If there is a
     return value in the form {"key": "value"} then it should be
     modeled as a TypedDict. If the "json" has too many key->value
     pairs, then it should be a class with the object as a property.
     In this case it is OK not to create a type for it. E.g. marc21!

## HTML
  - Follow project coding standard.
  - Only lowercase element names.
  - Avoid elements for layout porpose only.
  - Use HTML5 elements like section or article.
  - Don't use HTML elements for styling, use CSS instead.
  - Encapsulate views like records with an element. (e.g. <div>)

## Commits
  - After the commit the code should still work.
    - Check tests before commit!
  - Single responsibility:
    - if there is an "and" in the head then it should be more than one
      commit
    - don't mix refactoring with new functionalities
    - to be clear: it is highly possible that a commit has only one 
      line changed in the diff and the commit message has multiple
      paragraphs to explain why this change happened
  - Expressive commit messages:
    - explain what was wrong
    - explain why changes happend
    - explain how things are done
    - reference design decisions
  - Less than 80 characters
  - Commit message head and body separated by white line

## Merge
  - Create personal repository on github and create for every change
    on the main repository a pull request
  - Which has to be reviewed

## Workflows
### Make changes
  - Create an issue in the original repository
  - Implement that specific issue in your personal repository
  - Create a pull request with reference to that issue and a short
    description what has been done in this pull request
  - loop while !isPositivelyReviewed
    - the person responsible for the repository should review
      the pull request
    - apply possible change suggestions
    - add possible changes
  - Whe responsible person of the repository merges the pull request
    and closes the issue. This person uses the pull request
    description to add it to the merge description.
