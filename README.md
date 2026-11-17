# supportteam

## Flowsmith: workflow automation editor

`index.html` is a self-contained, n8n-style visual workflow builder. Open it in a browser; there is no build step or server.

```bash
python3 -m http.server 8000   # then visit http://localhost:8000
```

**What it does**

- Drag nodes from the library (or double-click the canvas) and wire outputs to inputs.
- Execute the workflow and inspect every node's input and output as a table or JSON.
- Expressions: `{{ $json.field }}` in any text field, `$node['Name'].json` for other nodes.
- Templates: support ticket triage, lead scoring webhook, API fetch, weekly revenue report.
- Import/export workflows as JSON. Work is saved to the browser automatically. Undo with Ctrl+Z.

**Nodes:** Manual Trigger, Schedule, Webhook, HTTP Request, Sample Data, Edit Fields, If, Switch, Filter, Merge, Wait, Code (JavaScript), Sort, Limit, Summarize, Output.

Schedule and Webhook triggers fire once when you execute in the editor; there is no backend running them on a timer or listening for real requests. HTTP Request calls real APIs from the browser, so the target must allow cross-origin requests.
