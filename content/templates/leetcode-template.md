<% tp.file.include("[[leetcode-frontmatter]]") %>
<%* let title = tp.file.title
  if (title.startsWith("Untitled")) {
    title = await tp.system.prompt("Title");
    await tp.file.rename(title);
  }
-%>
<%*
  let result= title.replace(/[_-]/g, ' ');
  result = result.replace(/\b\w/g, c => c.toUpperCase());
%>

# <% result %>

```python
<% tp.file.cursor(0) %>
```

```dataview
table without id file.inlinks as Backlinks
where file.name = this.file.name
```

## Related.

## References.

Categories::
