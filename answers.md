# Assignment: Build and Call Your Own MCP Tool

## 1. How many tools did the server list in Part 1, and how many in Part 3? What did you have to change in the client to make the new tool appear?

In Part 1, the server listed 8 tools. In Part 3, it listed 9 tools after I added the new `predict_both` tool to the MCP server.

I did not have to make any changes to the client to register the new tool. The client automatically discovered it by calling `server.list_tools()`. This demonstrates that MCP clients can dynamically discover tools provided by a server.

## 2. On how many of the 114 test patients do the two models disagree? For each of those patients, which model was right?

The two models disagreed on 8 out of 114 test patients.

For each disagreement, I compared the predictions from Logistic Regression and KNN with the patient's actual class. The model whose prediction matched the actual class was considered correct.

**Patient results:**

Logistic Regression correct: 7 patients
KNN correct: 1 patient

## 3. Overall, which model was right more often when they disagreed?

Logistic Regression was right more often when the models disagreed.

Out of the 8 disagreement cases:

Logistic Regression was correct 7 times
KNN was correct 1 time

This indicates that Logistic Regression made the better prediction in most of the cases where the two models produced different results.
## 4. In your own words: why does the description in triple quotes (`"""..."""`) matter when an AI app uses this tool?

The description in triple quotes is important because it explains what the tool does. An AI application can read this description to understand the purpose of the tool and decide when it should be used. A clear description helps the AI select the correct tool when responding to a user's request.

## 5. Why is it useful for the server to log every tool call?

Logging every tool call is useful because it creates a record of what happened on the server. It helps developers track which tools were used, identify errors, troubleshoot problems, and monitor activity. Request IDs also make it easier to trace individual requests and understand what happened during execution.