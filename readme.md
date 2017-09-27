# Drupal CD Example Module

This module is meant as an example of a continious delivery module for Drupal 7.

You can refer to further reading on this subject here:
	- https://www.drupal.org/docs/7/creating-custom-modules/howtos/examples-for-database-update-scripts-using-hook_update_n-how
	- http://blog.dcycle.com/blog/46/continuous-deployment-drupal-style/

### How to Use This Module

	- Install on any Drupal 7 system, drush install drupal_cd -y
	- Modify the .install file with additional _update hooks for any custom action
		that cannot be accomplished via features or strongarm.
	- You may use batch operations for these _update hooks, please take this
		into consideration.
	- When you find yourself repeating certain logic, add a helper function to
		the .module file
	- Please make sure to write tests for any additional functionality and to
		test each additional _update hook accordingly.
	- For testing and integration purposes refer to the Drupal_CI module.
