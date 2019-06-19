# Substance Lab Playbook

Hi!

We are Substance Lab. We craft awesome web software for picky customers.

This is our playbook. It describes how we work, and how we make our customers and their projects successful.

We have decided to open this with the world because we believe in sharing. If you like what you see and especially if you use any of the ideas described here, feel free to let us know.

## Weekly structure

We're a consultancy; doing client work is our primary focus.

We schedule projects on a daily basis so we can focus on one project each day, not having to context switch between multiple projects. If possible, we’ll schedule multiple, successive days for the same project.

We start each week with a team-wide status meeting where we take a look at the schedule for the week and everybody is kept up to date on new leads and sales and general announcements.

### Geek days

We’re geeks and we thrive on playing, experimenting and building. This means we work 4 days of the week on client work, while the last day (typically Friday) is for geek days.

If a week has less than five days due to personal time, vacations, holidays, sick leave, the geek day for that week is skipped.

Geek days should be used for stuff that is somewhat related to the business or to self improvement. This could be

* Contributing to an open source project (you can find contribution suggestions on [Code Triage](https://www.codetriage.com/))
* Creating an open source project
* Writing a blog post
* Learning a new technology
* Optimizing a workflow
* Improving internal tools
* Preparing presentations for user groups or conferences
* Helping people on [Stack Overflow](http://stackoverflow.com), [Exercism](http://exercism.io/) or elsewhere.


### Single Day Products

Every so often we'll use an investment day to build something, anything. The rule: It must be built and launched in a single day. Planning it beforehand is acceptable, though, and probably a good idea. We keep a list of [Single Day Product Ideas](https://github.com/substancelab/ideas/issues) where we hash out ideas.


## Workflow

### master is always deployable

The master branch is our main branch. It is always working and deployable so we can confidently base future work on it.

### Branches

Don’t commit directly to master. Create a branch for whatever you’re doing, make your changes and commits on that branch.

### Run all tests on the branch

When making changes make sure you run all the tests in the test suite, not just the ones you think you might have impacted.

### Run tests on pushes

The full test suite should be run on CI whenever changes are pushed to remote branches.

### Perform code reviews before merging to master

When your changes are ready to be reviewed, create a pull request for the branch. When your pull request is complete ask for reviews from the other members of your team by using GitHubs "Request review" feature or GitLabs "Assign approver".

### Keep commits focused and complete

See [The Anatomy of a Good Commit](https://mentalized.net/journal/2018/12/12/anatomy-of-a-good-commit/) for guidelines of how and why to create good commits.

* If you feel the need to put "and" in your commit message, the commit is probably too big.
* If you find it difficult describing what your commit does, it's probably too big.
* If you find it difficult describing the "why" of your changes, your commit might be too small.

### Commit messages tell intent

Explaining what you did is nice, explaining why you did it is even nicer. It’s even more useful if you explain why you did it over other options.

See [How to Write a Git Commit Message](http://chris.beams.io/posts/git-commit/) for an overview of how to write (and why) good commit messages. In summary:

1. Separate subject from body with a blank line
2. Limit the subject line to 50 characters
3. Capitalize the subject line
4. Do not end the subject line with a period
5. Use the imperative mood in the subject line
6. Wrap the body at 72 characters
7. Use the body to explain what and why vs. how

### Example: Building a feature

Grab the most important, ready story from the project management tool (GitHub, Waffle, whatever your project uses). Assign it to yourself and…

    $ git checkout master
    $ git pull
    $ git checkout --branch ISSUE_NUMBER-ISSUE_DESCRIPTION

… make your changes and commit each change in small, atomic commits. When done …

    $ git pull
    $ git rebase —interactive master
    $ git push --set-upstream origin

Create a pull request on GitHub.

### Example: Fixing a bug

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

* Colors are always 6-digit, lowercase hex (ie `#abcdef`), unless we need the alpha channel, in case rgba is used.
* Rules, selectors are placed in alphabetical order as much as possible.
* Place used mixins at the top to make it possible to overwrite their values.

## Common scripts

We strive to include a set of scripts in all repositories that gives a uniform way of performing common development tasks across projects, frameworks, and languages.

* `script/deploy`: Deploys the application to production (usually).
* `script/run`: Launches the application for local development.
* `script/update`: Ensures application dependencies are installed and upgraded, and that the application is otherwise in pristine order for development.

## Sales process

New customers are tracked on our Sales board in Trello.

1. Leads - Someone contacts us.
2. Contacted - Initial followup with a questionnaire.
3. Meeting - We have a phone call or have them come into the office.
4. Estimate
5. Proposal sent
6. Won/Lost

## Yearly charitable donation

At the beginning of each year, when the results from the year prior are done, we donate 10% of the yearly result to a given charity. The charity is chosen each year by all of us based on suggestions and votes from all employees.
