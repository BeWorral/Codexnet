## Workflow
The file `n8n-flow.json` defines an n8n workflow that starts with a Webhook node. It listens for POST requests on the path `woocommerce-order-completed` when a WooCommerce order is completed.

Each day the workflow sends a WhatsApp message through an HTTP request node. On days 1, 3, 5, 9, 14 and 15, it also sends an email using another HTTP request node. A Wait node pauses the workflow for one day before moving to the next day, continuing this pattern until the final email on day 15.

To keep merges simple, the workflow identifies its nodes only by their names rather than numeric `id` values.
