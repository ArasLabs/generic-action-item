# Generic Action Item with Workflow and Templates

Adds an item type "gAction Item" with a simple workflow that can be re-used on any item type to add action item lists.

Many times when creating a custom workflow and its form in Aras Innovator or when extending existing processes there can be a requirement to have sub-workflows to follow-up on additional actions or “ToDo’s”. Of course, these sub-workflows then have to be created “ad-hoc”. A common way here is to add a relationship listing actions to do and there point to an item with a workflow, so it shows in the InBasket of an action’s owner.

This solution package will exactly address this.

## History

This project and the following release notes have been migrated from the old Aras Projects page. Unlike community projects that have been migrated and archived, this project will be updated for compatibility with the latest release of Aras Innovator.

Release | Notes
--------|--------
[v2.0.1](https://github.com/ArasLabs/generic-action-item/releases/tag/v2.0.1) | Readme usage updated. Tested on 11 SP12, 11 SP15.
[v2](https://github.com/ArasLabs/generic-action-item/releases/tag/v2) | Generic Action Item Solution package and Documentation for Aras 10 + 11
[v1](https://github.com/ArasLabs/generic-action-item/releases/tag/v1) | Generic Action Item Solution package and Documentation

#### Supported Aras Versions

Project | Aras
--------|------
[v2.0.1](https://github.com/ArasLabs/generic-action-item/releases/tag/v2.0.1) | 10 SPx, 11 SPx
[v2](https://github.com/ArasLabs/generic-action-item/releases/tag/v2) | 10 SPx, 11 SPx
[v1](https://github.com/ArasLabs/generic-action-item/releases/tag/v1) | 9.3 SPx, 9.4 SPx

## Installation

#### Important!
**Always back up your code tree and database before applying an import package or code tree patch!**

### Pre-requisites

1. Aras Innovator installed (version 11.0 SPx preferred)
2. Aras Package Import tool
3. GenericActionItem import packages

### Install Steps

1. Backup your database and store the BAK file in a safe place.
2. Open up the Aras Package Import tool.
3. Enter your login credentials and click **Login**
  * _Note: You must login as root for the package import to succeed!_
4. Enter the package name in the TargetRelease field.
  * Optional: Enter a description in the Description field.
5. Enter the path to your local `..\GenericActionItem\Import\1-Import - Generic Action Item Functions\imports (admin).mf` file in the Manifest File field.
6. Select **generic Action Item** in the Available for Import field.
7. Select Type = **Merge** and Mode = **Thorough Mode**.
8. Click **Import** in the top left corner.
9. Optional: Repeat steps 5-8 for `..\GenericActionItem\Import\2-Import - Example on DCO (optional)\1-Import\imports (admin).mf`.
10. Optional: Repeat steps 5-8 for `..\GenericActionItem\Import\2-Import - Example on DCO (optional)\2-Import\imports (admin).mf`.
11. Optional: Repeat steps 5-8 for `..\GenericActionItem\Import\3-Import - Example Action Item Template (optional)\imports (admin).mf`.
12. Close the Aras Package Import tool.

## Usage
This package can be used one of two ways:
* Use an Action Item Template set up by an Administrator
* Add to an existing DCO item by a user, either as ad-hoc or by using an existing template as above.

> This item may also be configured as a relationship to other items, but must be set to a Create New type of relationship.

###Example Usage: 
1. (Optional) Create Template(s) for action items.
2. Create or open an Express DCO.
  * If the item is new, save item before using template action.
3. Use Action to add from template or add ad hoc using tab
4. Fire workflow for action using RMB action in search grid/tab
5. Complete action items via inbasket (closing item will require user password)
  * If notes are needed to close, add to action item via RMB view command.

> See [generic Action Item Concepts v1-2(A10).pdf](./Documentation/generic%20Action%20Item%20Concepts%20v1-2(A10).pdf) for more information on using this project.

## Contributing

1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -am 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request

For more information on contributing to this project, another Aras Labs project, or any Aras Community project, shoot us an email at araslabs@aras.com.

## Credits

Created by Rolf Laudenbach for Aras Corporation.

## License

Aras Labs projects are published to Github under the MIT license. See the [LICENSE file](./LICENSE.md) for license rights and limitations.
