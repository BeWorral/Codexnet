## Workflow
The file `n8n-flow.json` defines an n8n workflow triggered by a POST webhook on the path `woocommerce-order-completed`.
It sends a WhatsApp message via an HTTP request every day for 15 days and on days 1, 3, 5, 9, 14 and 15 it also sends an email via another HTTP request node.
A Wait node keeps one-day pauses between each day until the workflow finishes after day 15.
