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

![file-PAxK0uGU7C.png](https://stoplight.io/api/v1/projects/cHJqOjEyNDcxMw/images/sgP0EXlLSrA)

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