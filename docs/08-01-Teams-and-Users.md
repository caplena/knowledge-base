---
stoplight-id: c7crk1hsev913
---

# Teams and Users - User Management

## How Permissions Work

Permissions can be defined on two levels:

- Through roles (valid for all projects belonging to your organization)
- per object (project / dashboard)

**Example**: A user might have the right to view and inherit from all projects, but only edit specific ones.

Permissions are only additive, meaning that permissions that are granted through roles **can not be revoked** on a per-project basis.

**Example**: When a user has the role "All Data Access", allowing him or her to see and edit the projects of all team members, this permission cannot be revoked for single projects.

## Special Permissions

There are two special classes of users, whose permissions cannot be changed:

1. **Object owners**: The user that uploaded a project initially or created a dashboard will always have all permissions on this object (except if it is transferred).
2. **Company administrator**: The root account of an organization will always have all permissions on all objects.

## Changing a User's Role

To change the role of a user, navigate to your account page and click the "Team" section. Then choose a new role from the dropdown for the user.

![Bildschirmfoto 2023-03-20 um 09.46.47.png](<../assets/images/Bildschirmfoto 2023-03-20 um 09.46.47.png>)

### User Roles Available

Six different roles are available, allowing you to tailor access levels for your teams and beyond.

#### External Topic Assignment

*No upload capability; No access to projects or Dashboards of others by default.*

Detailed permissions: The user can
* execute all actions on objects where they are the owner, e.g. on projects they uploaded themselves.

#### Administrator
*Access to the projects, questions and dashboards of all users; Team and subscription management permissions.*

Detailed permissions: The user can
* append rows to all projects of the organization.
* delete all projects of the organization.
* manage the subscription of the organization.
* edit all projects of the organization.
* download all projects of the organization.
* view all projects of the organization.
* inherit from all projects of the organization.
* create new projects.
* change permissions on all projects of the organization.
* view all dashboards of the organization
* edit and delete all dashboards of the organization
* manage the team / accounts of the organisation
* use the connected integrations (e.g. Qualtrics) of all users in the organization.
* edit & delete the connected integrations (e.g. Qualtrics) of all users in the organization.
* view additional (Meta-)data for individual rows in dashboards of the organization
* execute all actions on objects where they are the owner, e.g. on projects they uploaded themselves.

#### Full Data Access
*Upload capability; Access to projects & dashboards of all team members.*

Detailed permissions: The user can
* append rows to all projects of the organization.
* delete all projects of the organization.
* edit all projects of the organization.
* download all projects of the organization.
* view all projects of the organization.
* inherit from all projects of the organization.
* create new projects.
* change permissions on all projects of the organization.
* view all dashboards of the organization
* edit and delete all dashboards of the organization
* use the connected integrations (e.g. Qualtrics) of all users in the organization
* view additional (Meta-)data for individual rows in dashboards of the organization
* execute all actions on objects where they are the owner, e.g. on projects they uploaded themselves.

#### Project Manager
*Upload capability; Only full access to projects created by oneself, but access to all topics collections and fine-tuned AI's from all team members.*

Detailed permissions: The user can
* create new projects.
* inherit from all projects of the organization.
* view additional (Meta-)data for individual rows in dashboards of the organization
* execute all actions on objects where they are the owner, e.g. on projects they uploaded themselves.

#### Internal analyst
*No upload capability; Permission to edit and access projects of all team members, but no permission to download projects and no access to Dashboards of others.*
Detailed permissions: The user can
* edit all projects of the organization.
* view all projects of the organization.
* inherit from all projects of the organization.
* view additional (Meta-)data for individual rows in dashboards of the organization
* execute all actions on objects where they are the owner, e.g. on projects they uploaded themselves.

#### Analyst
*No upload capability; Permission to view and visualize projects of all team members, but no permission to edit no download any projects.*
Detailed permissions: The user can
* view all projects of the organization.
* view additional (Meta-)data for individual rows in dashboards of the organization
* view all dashboards of the organization
* execute all actions on objects where they are the owner, e.g. on projects they uploaded themselves.

## Changing Project-Specific Permissions

The per-project permissions can be defined when entering your project from the project list: Click on the project that you would like to edit and then click on the icon with two people from the *Project actions*.

![Bildschirmfoto 2022-06-13 um 19.38.47.png](https://stoplight.io/api/v1/projects/cHJqOjEyNDcxMw/images/5otYMbhbPOU)

## Changing the Owner of a Project / Dashboard

An object usually belongs to the user that has created it. If you want to change ownership of a project, e.g. because someone has left your team, you can change the ownership of items manually: First open the Permission dialog, as described in the section above. Then click the "Make owner" button while having the new owner selected:

![Bildschirmfoto 2022-06-13 um 19.40.28.png](https://stoplight.io/api/v1/projects/cHJqOjEyNDcxMw/images/EkurlT8nMI0)

**Note**: When changing the ownership of a project, this will also change the owner of all questions belonging to that project. Similarly, changing the owner of a dashboard will change the owner of all contained charts.

**When deleting the account of a team member, you have the option to automatically transfer all his/her remaining projects to the root user.**

## Why can't I change Permissions of a Project

If you can't see the permissions icon at all, this means you are not part of an organization with permissions enabled.

If the permissions icon is greyed out, this can have multiple reasons:
- You have selected multiple projects: Permissions can only be edited for one project at the time. Make sure you have only selected one checkbox.
- You don't have the permission to change the permissions of this project.

If the permission dialog opens, but you are not able to edit specific fields, this means those permissions cannot be changed. Reasons for that might be:

- Organization-wide permissions: It is only possible to grant additional permissions on a per-project level. You cannot revoke organization-wide permissions for one project. See the first paragraph of this article.
- Project owners and company administrators always have all permissions on a project.