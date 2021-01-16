---
{{frontmatter}}
---

{{description}}

+++

Revisions:
================================================================================

Key: 🟣 - published        🟢 - accepted         🟠 - needs-review     🔵 - draft
     🔴 - changes-planned  🔨 - needs-revision   🛫 - abandoned


--------------------------------------------------------------------------------
{% for rev in task.revisions %}
{{rev.name}} - {{utils.get_status_symbol(rev.status)}} - {{rev.title}}
{% endfor %}
--------------------------------------------------------------------------------

Comments:
================================================================================

{% for c in task.comments|reverse %}
{{utils.justify_strings(c.author.name + " ({})".format(c.author.username), c.created, 80)}}
--------------------------------------------------------------------------------

{{c.text}}

{% endfor %}

::: Add Comment
--------------------------------------------------------------------------------


+++