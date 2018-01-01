
# Drupal Accessibility Quicksheet #

*Maintained by Mike Gifford,  Drupal 8 Core Accessibility Maintainer*

## How Does Drupal accessibility Work?
- Drupal Core is leveraged by every module & theme on Drupal.org. The central APIs are critical in setting good standard defaults which are inherited by sites built with it. This does not mean that all modules or themes are equally accessible, as individual developers may overlook or turn off best practices that are defined in Core. It simply sets default states which can be either ignored or overridden by the maintainer of the code. 
- The Drupal community has been striving for WCAG 2.0 AA since Drupal 7 for both public and administration pages. In Drupal 8 we took on finding ways to incorporate elements of [ATAG 2.0 AA, Part A & B](https://www.drupal.org/project/issues/search?issue_tags=atag). The accessibility team is now looking for ways to address [WCAG 2.1 AA recommendations](https://www.drupal.org/project/issues/search?issue_tags=wcag21) into our code base. 
- Despite the accessibility targets that the Drupal community is setting, the code is not completely WCAG 2.0 AA compliant. That said, we have yet to find a more compliant enterprise CMS that is actively being developed and maintained. 
- Drupal has several central accessibility features in Drupal 8. Having a central solution to display:none;, managing tab indexes as well as aria-live allows best practices to evolve with a complex ecosystem of software on the internet. The simplest of these allows for a set of CSS classes which controls how content is hidden but visible for screen-readers, keyboard only users or nobody at all. This simple set of classes is still in flux and has been discussed by accessibility experts for at least a decade. 
- Learn about accessibility [features we've brought into Drupal Core](https://www.drupal.org/about/features/accessibility)

## If You Have a Drupal Site and Want to Increase its Accessibility
- For D8 sites, take a look at [these contributed modules which may help extend your site's accessibility](https://www.drupal.org/node/2913360) 
- For D7 sites, take a look at [these contributed modules which may help extend your site's accessibility](https://www.drupal.org/node/394252) 
- Review existing [Drupal Accessibility Best Practices guide](https://www.drupal.org/docs/7/accessibility/tools-and-best-practices)
- Review this document to learn how to [hide content properly](https://www.drupal.org/docs/8/accessibility/hide-content-properly)
- Like every other site, take a look at it with automated tools like [Tenon](https://tenon.io/) & [WAVE](http://wave.webaim.org/). Do keyboard only testing. It is most likely, that if you find an accessibility error, it wasn't there in the source code. This definitely isn't always the case though. If you find an error that you think is in a Drupal module or theme ... report it in the appropriate project issue queue. 
You can even test it out modules & themes in a vanilla testing environment on https://simplytest.me if you want to be sure. 

## If you Want to Contribute to Drupal Accessibility
- Make sure you have an account on Drupal.org so that you can post issues and contribute to nudging ahead issues you care about.
- Join the [Accessibility Channel on Drupal Slack Group](https://www.drupal.org/slack) - it is a great community of folks who can help.
- Look to see if you can contribute to issues in the [accessibility issue queue](https://www.drupal.org/project/issues/search?issue_tags=accessibility) - there are lots of issues, and many of them need to be tested to verify that the patch provided fixes the problem described. 
- If you've found a way to make your site more accessible, see if you can't find some way to contribute that back to the community. Maybe you have a great module which helps to evaluate Alt Text to integrate with a machine learning algorithm to get rid of garbage text. Every user has access to a sandbox where they can share code, but you can also simply share it on GitHub and tell folks about it on the Slack Channel above. 

### Requests from the Drupal Accessibility Team ###
- We need help with unit testing for accessibility issues in Drupal. If you've got mad skills at this, we need your experience to help write better tests to verify that accessibility is maintained.
- We need help with automated testing tools. Ideally every aspect of Drupal Core and all Contributed modules & themes will go through automated accessibility testing. Tools like axe-core can do this, but it requires additional integration.
- We need more testers. We particularly want users who can test with Dragon Naturally Speaking. Aural interfaces are going to be particularly important for websites, but the Drupal Community does not have a lot of experience building aurally pleasing interfaces. 
- We use Drupal.announce() in Drupal Core, but we need to use it a lot more. Modules & themes in Contrib both need better use of this JavaScript class to consistently integrate aria-live implementations. 
- We don't know what we don't know. Please tell us what we are missing.

See [Challenges section of the GPII DeveloperSpace](https://ds.gpii.net/challenges) for more information on these challenges
