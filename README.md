This tutorial is realized using grails 2.4.2

Tutorial steps are "cristalyzed" in branches. The main branch corresponds to the completed application.

1.Initialize spud environment:
 1. Add spud dependencies to BuildConfig.groovy
 2. Link dashboard in main layout adding ```<g:link controller="dashboard" namespace="spud_admin">Spud Dashboard</g:link>``` in main.gsp
 3. Browse to http://localhost:8080/spud-tutorial/spud/admin
 4. You will be redirected to the setup wizard where you can define the first cms administrator

2. Adding a footer:
 1. Add the spud manifesf with the template name in main.gsp 
 ```html
 <%
//= template_name Simple
%>
```
 2. Add the footer snippet reference ```<sp:snippet name="Footer" />``` in main.gsp
 3. Browse to dashboard and define a footer snippet named "Footer"

3. Adding a menu:
 1. Add the manu reference tag ```<sp:menu name="Main " id="navigation"/>``` in main.gsp
 2. Browse to dashboard and define a menu named "Main"

4. Adding a editable page:
 1. Define home as a cms template in Config.groovy
 ```groovy
 	spud {
		cms {
			rootPageName = "home"
			defaultLayout = "main"
			cacheEnabled = false //Turn on action caching
		}
	}
```
 2. Add ```<g:pageProperty name="page.body" />``` in main.gsp
 3. Add ```${page?.name}``` in <g:layoutTitle>
 4. Add ```//= html body``` in main.gsp spud manifest 
 
