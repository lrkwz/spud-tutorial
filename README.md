This tutorial is realized using grails 2.4.2

Tutorial steps are "cristalyzed" in branches. The main branch corresponds to the completed application.

1. Add spud dependencies to BuildConfig.groovy and link dashboard in main layout; then:
1.1 Browse to http://localhost:8080/spud-tutorial/spud/admin
1.2 You will be redirected to the setup wizard where you can define the first cms administrator
2. Adding a footer:
2.1 Add template definition to main layout
2.2 Add the footer snippet reference in main.gsp
2.2 Browse to dashboard and define a footer snippet
3. Adding a menu:
3.1 Add the manu reference tag <sp:menu name="Main " id="navigation"/>in main.gsp
3.2 Browse to dashboard and define a menu named "Main"
4. Adding a editable page
