---
{"dg-publish":true,"permalink":"/20-definitions/chef/","tags":["defs_ccna"]}
---

#### Chef
##### KEY Summary
- Written in Ruby
- Agent Based
- Pull model
- TCP 10002 to send configs to clients
- Its files (e.g., Recipes and Cookbooks) use a [[20 - Definitions/Domain-Specific Language\|DSL]] based on Ruby

##### Broad Summary
- Written in ruby
- Chef is agent-based
- Uses a Pull model
- Server uses [[20 - Definitions/TCP\|TCP]] 10002 to send configurations to client
- Files use a [[20 - Definitions/Domain-Specific Language\|DSL (Domain-Specific Language)]] based on Ruby
- Key files
	- Resources
		- The "Ingredients" in a recipe
		- Configuration objects managed by Chef
	- Recipes
		- The "Recipes" in a cookbook
		- Outline the logic and actions of the tasks performed on the resources
	- Cookbooks
		- A set of related recipes grouped together
	- Run-list
		- An ordered list of recipes that are run to bring a device to the desired configuration state

![Chef-2.png](/img/user/CCNA/Attachments/Chef-2.png)
Image courtesy of [Chef Infra Overview](https://docs.chef.io/chef_overview/)





# Metadata
### OSI or TCP/IP Layer

### CCNA Exam Topic

### Contributors

### Sources
[Chef Infra Overview](https://docs.chef.io/chef_overview/)