# Contributing

When contributing to this repository, please first discuss the change you wish to make via issue,
email, or any other method with the owners of this repository before making a change. 

Please note we have a code of conduct, please follow it in all your interactions with the project.

## Pull Request Process

1. Ensure that you have tested your archetype locally by generating a project from your archetype. A guide can be found as README.md in branch [mvn-archetypes](https://github.com/lycano/cryofall-mod-templates/tree/mvn-archetypes).
2. Keep the mod template simple. Don't add too much complexity to the mod if its not needed. The archetype should be seen as a starter package not an actual mod.
3. Add Placeholder methods if they are needed and keep them empty. For example if the template should consume an event the subscribed method should be empty and should include a descriptive comment to explain what this method shall be used for.
4. When adding new properties to a template add a description when making a pull request. I will add a pull request template so you dont have to worry about detail that much.
5. Increase the version numbers in your pom.xml when needed. Use SNAPSHOT suffix in pom.xml version tag if you think your template is not fully ready yet otherwise just use version numbers like 1.0. See #Versioning for further details.

## Code of Conduct

### Our Pledge

In the interest of providing resources to get you as the CryoFall Mod Developer
started in creating your mod, we as contributors and maintainers pledge to
keep track of the contributed work and update or extend the mod template as needed.

### Our Standards

You as a contributor may or may not add your template to the repository,
discuss new features or bugs via issue. If a mod may not meet the criteria beeing a template e.g.
is an actual mod that you would like add to this repository the pull might be closed.

Please refrain from acting negative. Keep up a positive environment
this includes:

* Using welcoming and inclusive language
* Being respectful of differing viewpoints and experiences
* Gracefully accepting constructive criticism
* Focusing on what is best for the project
* Showing empathy towards other project members

Examples of unacceptable behavior by participants include:

* The use of sexualized language or imagery and unwelcome sexual attention or
advances
* Trolling, insulting/derogatory comments, and personal or political attacks
* Public or private harassment
* Publishing others' private information, such as a physical or electronic
  address, without explicit permission
* Other conduct which could reasonably be considered inappropriate in a
  professional setting

### Our Responsibilities

Project maintainers are responsible for clarifying the standards of acceptable
behavior and are expected to take appropriate and fair corrective action in
response to any instances of unacceptable behavior.

Project maintainers have the right and responsibility to remove, edit, or
reject comments, commits, code, wiki edits, issues, and other contributions
that are not aligned to this Code of Conduct, or to ban temporarily or
permanently any contributor for other behaviors that they deem inappropriate,
threatening, offensive, or harmful.

### Scope

This Code of Conduct applies both within project spaces and in public spaces
when an individual is representing the project or its community. Examples of
representing a project or community include using an official project e-mail
address, posting via an official social media account, or acting as an appointed
representative at an online or offline event. Representation of a project may be
further defined and clarified by project maintainers.

### Enforcement

Instances of abusive, harassing, or otherwise unacceptable behavior may be
reported by contacting the project team via email. All complaints will be reviewed
and investigated and will result in a response that
is deemed necessary and appropriate to the circumstances. The project team is
obligated to maintain confidentiality with regard to the reporter of an incident.
Further details of specific enforcement policies may be posted separately.

Project maintainers who do not follow or enforce the Code of Conduct in good
faith may face temporary or permanent repercussions as determined by other
members of the project's leadership.

### Attribution

This Code of Conduct is adapted from the [Contributor Covenant][homepage], version 1.4,
available at [http://contributor-covenant.org/version/1/4][version]

[homepage]: http://contributor-covenant.org
[version]: http://contributor-covenant.org/version/1/4/
