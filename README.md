# [OWASP BLT](https://www.bugheist.com) [![Build Status](https://travis-ci.org/OWASP/BLT.svg?branch=master)](https://travis-ci.org/OWASP/BLT) [![Codacy Badge](https://api.codacy.com/project/badge/Grade/5d899b7004cc44f1977b03bc7d664ad9)](https://www.codacy.com/project/souravbadami/BLT/dashboard?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=OWASP/BLT&amp;utm_campaign=Badge_Grade_Dashboard)

**Report issues and get points, companies are held accountable.**

Live Site: [Bugheist](http://bugheist.com/)

# Usage

## Bugheist Bug Reporting Plugin

A floating bug reporting button for your website which redirects back to Bugheist and help's users to report bug for that specific page. Just embed this script within body tag of your page to enable this plugin.

  ```
    <script type="text/javascript">
		var button = document.createElement("Button");
		button.style = "bottom:15px;left:15px;position:fixed;z-index: 12;border-radius:100%;background: url('https://www.bugheist.com/static/img/logo.0cc160e97934.png') no-repeat center; height: 50px; width: 50px; outline: none;background-size: 50px 50px;"
		document.body.appendChild(button);
		var url = window.location.href;
		var bugheist = 'https://www.bugheist.com/report/?url=' + url;
		button.onclick = function() {
			var redirectWindow = window.open(bugheist, '_blank');
            redirectWindow.location;
		}
	</script>
  ```

# Development

## Setting Up Development Server

Please follow the development server setup procedure [here](https://github.com/OWASP/BLT/wiki/Setting-up-the-development-server). Currently, development server can be installed using virtualenv or vagrant. You can also use pipenv install, pipenv shell and then continue with the remaining instructions.

## Coding style guide

Please follow the [pep8](http://pymbook.readthedocs.io/en/latest/pep8.html) code style for the project. It helps us in keeping the codebase consistent and improves readibility for other developers.

## License

The BLT code is released under [GNU Affero General Public License v3.0 (AGPL-3.0)](https://github.com/OWASP/BLT/blob/master/LICENSE.md).

## Resources

- Join the [OWASP Slack Channel](https://owasp.herokuapp.com/) and ask questions at **#project-blt** Github activity can be seen in **#blt-github**.

## Notes

- If you find a bug or have an improvement, use BLT to report it!
- Our staging server is now live at https://bugheist-staging.herokuapp.com/ - staging uses the master branch and we have review apps setup that deploy a new instance for each pull request. 
- for each new issue, create a new branch with issue-382 or similar matching the issue number - when you commit add fixes #288 to link the issue to the pull request
- After installing requirements run pipenv lock -r > requirements.txt to freeze them.
- Our Figma desins are also Open Source you can see them here https://www.figma.com/file/s0xuxeU6O2guoWEfA9OElZ/Bugheist-Full-Design to contribute to the design, add a pull request to the design changes file and we will merge them into our main figma file.
