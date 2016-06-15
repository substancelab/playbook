# Substance Lab Playbook

## Weekly structure

We're a consultancy; doing client work is our primary focus. However, we're also geeks, and playing/experimenting/building is what we thrive on. This means we work 4 days of the week on client work, while the last day (typically Friday) is for geek days.

If a week has less than five days due to personal time, vacations, holidays, sick leave, the geek day for that week is skipped.


### Geek days

Geek days should be used for stuff that is somewhat related to the business or to self improvement. This could be

* Contributing to an open source project
* Creating an open source project
* Writing a blog post
* Learning a new technology
* Optimizing a workflow
* Improving internal tools
* Preparing presentations for user groups or conferences
* Helping people on [Stack Overflow](http://stackoverflow.com), [Exercism](http://exercism.io/) or elsewhere.


### Single Day Products

Every so often we'll use an investment day to build something, anything. The rule: It must be built and launched in a single day. Planning it before that day is acceptable, though. We keep a list of [[Single Day Product Ideas]] where we has out the ideas.


## Workflow

### Bugfixes

    $ git checkout master
    $ git pull
    $ git checkout --branch ISSUE_NUMBER-ISSUE_DESCRIPTION

... make your changes and commit each change in small, atomic commits. When done ...

    $ git pull
    $ git rebase master
    $ git push --set-upstream origin

Create a pull request on GitHub.

## Development and languages

### Code styles

#### Ruby

We generally follow [GitHubs Ruby style guide](https://github.com/styleguide/ruby).

A [Rubocop configuration](https://github.com/substancelab/dotfiles/blob/master/rubocop.yml) is available as part of our dotfiles project.


#### CSS/Sass

We generally write CSS using the Sass syntax. We strive to adhere to the guidelines from [SMACSS](https://smacss.com/).

A few guidelines:

* Colors are always hex, unless we need the alpha channel, in case rgba is used.
* Rules, selectors are placed in alphabetical order as much as possible.
* Place used mixins at the top to make it possible to overwrite their values.

## Sales process

New customers are tracked on our Sales board in Trello.

1. Leads - Someone contacts us.
2. Contacted - Initial followup with a questionnaire.
3. Meeting - We have a phone call or have them come into the office.
4. Estimate
5. Proposal sent
6. Won/Lost
