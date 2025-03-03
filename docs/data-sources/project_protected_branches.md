---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "gitlab_project_protected_branches Data Source - terraform-provider-gitlab"
subcategory: ""
description: |-
  The gitlab_protected_branches data source allows details of the protected branches of a given project.
  Upstream API: GitLab REST API docs https://docs.gitlab.com/ee/api/protected_branches.html#list-protected-branches
---

# gitlab_project_protected_branches (Data Source)

The `gitlab_protected_branches` data source allows details of the protected branches of a given project.

**Upstream API**: [GitLab REST API docs](https://docs.gitlab.com/ee/api/protected_branches.html#list-protected-branches)

## Example Usage

```terraform
data "gitlab_project_protected_branches" "example" {
  project_id = 30
}

data "gitlab_project_protected_branches" "example" {
  project_id = "foo/bar/baz"
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Required

- `project_id` (String) The integer or path with namespace that uniquely identifies the project.

### Read-Only

- `id` (String) The ID of this resource.
- `protected_branches` (List of Object) A list of protected branches, as defined below. (see [below for nested schema](#nestedatt--protected_branches))

<a id="nestedatt--protected_branches"></a>
### Nested Schema for `protected_branches`

Read-Only:

- `allow_force_push` (Boolean)
- `code_owner_approval_required` (Boolean)
- `id` (Number)
- `merge_access_levels` (List of Object) (see [below for nested schema](#nestedobjatt--protected_branches--merge_access_levels))
- `name` (String)
- `push_access_levels` (List of Object) (see [below for nested schema](#nestedobjatt--protected_branches--push_access_levels))

<a id="nestedobjatt--protected_branches--merge_access_levels"></a>
### Nested Schema for `protected_branches.merge_access_levels`

Read-Only:

- `access_level` (String)
- `access_level_description` (String)
- `group_id` (Number)
- `user_id` (Number)


<a id="nestedobjatt--protected_branches--push_access_levels"></a>
### Nested Schema for `protected_branches.push_access_levels`

Read-Only:

- `access_level` (String)
- `access_level_description` (String)
- `group_id` (Number)
- `user_id` (Number)


