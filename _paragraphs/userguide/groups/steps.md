---
title: Steps to set up
book: userguide
chapter: groups
slug: group-access-steps
weight: 30
---

#### Steps for Group, User, and GroupUser group access configuration
1. Create **User resource** (or use existing default User resource)
   - Components
     - Email (Email component)
     - Password (Password component)

2. Create **Group resource**
   - Components
     - Name (Text component)

3. Create **GroupUser resource**
   - Components
     - Group (single Select / Resource component of Group resource submissions)
     - User (single Select / Resource component of User resource submissions)
     - `Note: both Group and User components in GroupUser resource can only be Single Selects. If you need one user to be assigned to multiple groups, you'll need to create multiple submissions of GroupUser resource`

4. Set up **Group assignment action** for the GroupUser resource
   - Select 'User' select as User setting and 'Group' select as Group setting
   ![](/assets/img/userguide/groups/group_assignment_action.png){: .img-fluid .img-thumbnail }

5. Create a **form with group access permissions**
   - Components
     - Group (single or multi Select / Resource component of Group resource submissions)
     - any other component you need
   - `Note: Group select on form with group access can be either single Select or multi Select depending on your needs - both should work`

6. Set up **Field Based Resource Access** for this form:
   - Select 'Group' component in one of the Read / Create / Write / Admin selects depending on which level of access you want to grant to a User. Read more about Field Based Resource Access levels in [Roles and Permissions section](../roles-and-permissions/#submissionpermissions).
   - `Note: when you change Field Based Resource Acccess setting, change only applies to new submissions you'll create after the change. Submissions created before the change would have level of acccess which was current on the time of their creation. For example: you didn't set up Filed Based Resource Access, created several submissions and then selected Group Resource on 'Read' level. Group users won't be able to see those several old submissions even if the group matches`
   
   ![](/assets/img/userguide/groups/field_based_resource_access.png){: .img-fluid .img-thumbnail }
