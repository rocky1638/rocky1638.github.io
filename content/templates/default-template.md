<% tp.file.include("[[default-frontmatter]]") %>
<%* let title = tp.file.title
  if (title.startsWith("Untitled")) {
    title = await tp.system.prompt("Title");
    await tp.file.rename(title);
  }
-%>
<%*
  const result= title.replace(/[_-]/g, ' ');
  // result = result.replace(/\b\w/g, c => c.toUpperCase());
%>

<% tp.file.cursor() %>

## references
