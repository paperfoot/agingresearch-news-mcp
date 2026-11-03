# Installing the AgingResearch.News MCP server

AgingResearch.News is a hosted remote MCP server. There is nothing to download, build or run, and no API key is needed for lookups.

1. Add a remote server named `agingresearch-news` with transport Streamable HTTP and this URL:

   ```text
   https://agingresearch.news/api/mcp
   ```

   Cline (`cline_mcp_settings.json`):

   ```json
   {
     "mcpServers": {
       "agingresearch-news": {
         "type": "streamableHttp",
         "url": "https://agingresearch.news/api/mcp",
         "disabled": false
       }
     }
   }
   ```

2. Check it works: call `search_papers` with `{"query": "cellular senescence"}`. It returns recent papers, each with its title, study type and link.

3. Optional: the account tools (`follow`, `unfollow`, `list_follows`, `list_questions`) and the Ask tools (`ask_arn`, `start_ultradeep`, `get_ask_answer`) ask the user to sign in through OAuth the first time they are called. The client opens the sign-in page; the user signs in or makes a free account, and the call goes through.

Lookups without an account are limited to a daily number; signed-in users get their own account's allowance.
