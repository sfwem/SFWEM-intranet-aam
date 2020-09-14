# SFWEM Intranet Resouces

The goals of this little project are two-fold:

1. Provide a simple, easy to update intranet website for the SFWEM network that can help point users to resources on the mesh.
2. Provide a local, SFWEM-based endpoint for AREDN Alert Messages.

Item #1 is pretty simple and dones't require a lot of magical sauce - create Jekyll site, add content, publish in docker on the mesh. Easy.

Item #2 is a little more complicated, though not much. Alerts can be generated using a custom collection, some fancy templates, and a lot of [liquid](https://jekyllrb.com/docs/liquid/). By writing a markdown file with some custom frontmatter and placing it in the `_alerts` folder, Jekyll will automatically generate properly formatted AAM messages. Mesh users can configure their nodes to pull alerts from the server by going to the Advanced Configuration page on their AREDN node, and setting `aredn.@alerts[0].localpath` to `http://sfwem.local.mesh/aam/`. Uniquely, a mechanism to link an Alert to a Bulletin (e.g. a blog post) with more detail on the Alert's content is provided, which will also help prevent alerts from becoming too long and clogging up a node's display.

Developer types can access a list of the current alerts via json at `/aam/alerts.json`, while `/aam/all/` will show you a rough HTML mockup of how nodes will display the alerts. AAM messages themselves are held in `/aam/all.txt`, as described in the AREDN docs.

In addition to the alerts displayed on nodes, you can view them via the `/alerts` page on the site itself. Each alert also has a dedicated page with full details and a JSON copy.

Powered by [Jekyll](https://jekyllrb.com/) using the [Lanyon theme](https://lanyon.getpoole.com/).