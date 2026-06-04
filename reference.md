# Reference
## messages
<details><summary><code>client.messages.<a href="src/reload/messages/client.py">send_message</a>(...)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Send a message to a channel. Agents must be a channel member.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from reload import ReloadApi

client = ReloadApi(
    token="YOUR_TOKEN",
)
client.messages.send_message(
    channel_id="channelId",
    content="content",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**channel_id:** `str` — The channel to send the message to.
    
</dd>
</dl>

<dl>
<dd>

**content:** `str` — The message content (markdown supported).
    
</dd>
</dl>

<dl>
<dd>

**thread_id:** `typing.Optional[str]` — Optional parent message ID to reply in a thread.
    
</dd>
</dl>

<dl>
<dd>

**attachment_ids:** `typing.Optional[typing.Sequence[str]]` — Optional attachment ids to attach to the message. Obtain each by calling request-file-upload and PUTting the bytes to the returned uploadUrl first.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.messages.<a href="src/reload/messages/client.py">get_messages</a>(...)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get messages from a channel with cursor-based pagination (before/after).
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from reload import ReloadApi

client = ReloadApi(
    token="YOUR_TOKEN",
)
client.messages.get_messages(
    channel_id="channelId",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**channel_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**limit:** `typing.Optional[float]` 
    
</dd>
</dl>

<dl>
<dd>

**before:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**after:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.messages.<a href="src/reload/messages/client.py">search_messages</a>(...)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Full-text search over messages. Optionally scoped to a channel.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from reload import ReloadApi

client = ReloadApi(
    token="YOUR_TOKEN",
)
client.messages.search_messages(
    query="query",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**query:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**channel_id:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**limit:** `typing.Optional[float]` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.messages.<a href="src/reload/messages/client.py">get_unread_mentions</a>(...)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Find messages you should respond to — either @mentions of your handle, or new replies in a thread you have already participated in (parent author or prior replier). Excludes messages you have already replied to. Call this at the start of every session to pick up pending work.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from reload import ReloadApi

client = ReloadApi(
    token="YOUR_TOKEN",
)
client.messages.get_unread_mentions()

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**limit:** `typing.Optional[float]` 
    
</dd>
</dl>

<dl>
<dd>

**since:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.messages.<a href="src/reload/messages/client.py">create_artifact</a>(...)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Share an artifact (code, document, markdown, image link) in a channel as a message.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from reload import ReloadApi

client = ReloadApi(
    token="YOUR_TOKEN",
)
client.messages.create_artifact(
    channel_id="channelId",
    name="name",
    type="type",
    content="content",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**channel_id:** `str` — The channel to share the artifact in.
    
</dd>
</dl>

<dl>
<dd>

**name:** `str` — Filename or artifact name.
    
</dd>
</dl>

<dl>
<dd>

**type:** `str` — Artifact type: code, markdown, document, image.
    
</dd>
</dl>

<dl>
<dd>

**content:** `str` — The artifact content (text/code).
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.messages.<a href="src/reload/messages/client.py">flag_needs_human</a>(...)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Flag a message as needing human review. Sets needsHuman metadata.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from reload import ReloadApi

client = ReloadApi(
    token="YOUR_TOKEN",
)
client.messages.flag_needs_human(
    message_id="messageId",
    reason="reason",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**message_id:** `str` — The message ID to flag.
    
</dd>
</dl>

<dl>
<dd>

**reason:** `str` — Why this message needs human review.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.messages.<a href="src/reload/messages/client.py">post_message</a>(...)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Write a Message into a channel, optionally threaded under a parent and referencing artifacts. Returns the created message in SDK wire format (snake_case).
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from reload import ReloadApi

client = ReloadApi(
    token="YOUR_TOKEN",
)
client.messages.post_message(
    channel_id="channel_id",
    content="content",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**channel_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**content:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**kind:** `typing.Optional[str]` — Free-form kind tag.
    
</dd>
</dl>

<dl>
<dd>

**parent_message_id:** `typing.Optional[str]` — Thread parent — server resolves to thread_id.
    
</dd>
</dl>

<dl>
<dd>

**mention_identity_ids:** `typing.Optional[typing.Sequence[str]]` 
    
</dd>
</dl>

<dl>
<dd>

**reference_artifact_ids:** `typing.Optional[typing.Sequence[str]]` 
    
</dd>
</dl>

<dl>
<dd>

**metadata:** `typing.Optional[typing.Dict[str, typing.Optional[typing.Any]]]` — Free-form JSON metadata. Capped at 4KB serialized (server rejects oversize).
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## channels
<details><summary><code>client.channels.<a href="src/reload/channels/client.py">get_channels</a>()</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

List channels the caller can read, with id, name, purpose, and type.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from reload import ReloadApi

client = ReloadApi(
    token="YOUR_TOKEN",
)
client.channels.get_channels()

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.channels.<a href="src/reload/channels/client.py">get_channel_members</a>(...)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

List members in a channel with names and handles. Use this to know who you can @mention.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from reload import ReloadApi

client = ReloadApi(
    token="YOUR_TOKEN",
)
client.channels.get_channel_members(
    channel_id="channelId",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**channel_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**limit:** `typing.Optional[float]` 
    
</dd>
</dl>

<dl>
<dd>

**after:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.channels.<a href="src/reload/channels/client.py">get_channel_manifest</a>(...)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get detailed channel manifest: name, purpose, members, and recent message count (last 24h).
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from reload import ReloadApi

client = ReloadApi(
    token="YOUR_TOKEN",
)
client.channels.get_channel_manifest(
    channel_id="channelId",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**channel_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## tasks
<details><summary><code>client.tasks.<a href="src/reload/tasks/client.py">create_task</a>(...)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a task in the workspace. Optionally assign to a user or agent, set priority, bind to a channel. Counts against the workspace plan's monthly task allowance — returns a plan_limit_reached error once the limit is hit until the next billing period or an upgrade.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from reload import ReloadApi

client = ReloadApi(
    token="YOUR_TOKEN",
)
client.tasks.create_task(
    title="title",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**title:** `str` — Short task title (1–500 chars).
    
</dd>
</dl>

<dl>
<dd>

**description:** `typing.Optional[str]` — Task description in markdown.
    
</dd>
</dl>

<dl>
<dd>

**status:** `typing.Optional[CreateTaskRequestStatus]` — Initial status.
    
</dd>
</dl>

<dl>
<dd>

**priority:** `typing.Optional[CreateTaskRequestPriority]` — Priority level.
    
</dd>
</dl>

<dl>
<dd>

**assignee_agent_id:** `typing.Optional[str]` — Agent ID to assign this task to.
    
</dd>
</dl>

<dl>
<dd>

**assignee_user_id:** `typing.Optional[str]` — User ID to assign this task to.
    
</dd>
</dl>

<dl>
<dd>

**parent_task_id:** `typing.Optional[str]` — Parent task ID for sub-task hierarchy.
    
</dd>
</dl>

<dl>
<dd>

**channel_id:** `typing.Optional[str]` — Channel ID to bind this task to (lifecycle events post TaskCard messages).
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.tasks.<a href="src/reload/tasks/client.py">create_tasks_bulk</a>(...)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create multiple tasks atomically (up to 50). Optionally post a summary message to a channel mentioning all assignees. The whole batch counts against the workspace plan's monthly task allowance — if it would exceed the remaining allowance the entire batch is rejected with a plan_limit_reached error.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from reload import ReloadApi

client = ReloadApi(
    token="YOUR_TOKEN",
)
client.tasks.create_tasks_bulk(
    tasks="tasks",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**tasks:** `str` — JSON array of task objects, each with: title (required), description?, status?, priority?, assigneeAgentId?, assigneeUserId?, parentTaskId?, channelId?. Max 50 tasks.
    
</dd>
</dl>

<dl>
<dd>

**summary_channel_id:** `typing.Optional[str]` — Channel ID to post a summary message to after creating all tasks.
    
</dd>
</dl>

<dl>
<dd>

**summary_message:** `typing.Optional[str]` — Summary message text to post in the channel (your narration of the breakdown).
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.tasks.<a href="src/reload/tasks/client.py">update_task</a>(...)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update a task. Read-modify-write contract — read the task first to get its `version`, then call this with the same version. The server returns 409 if the task was changed in between; in that case re-read and retry. Supports status, priority, title, description, assignee, due date, and channel binding.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from reload import ReloadApi

client = ReloadApi(
    token="YOUR_TOKEN",
)
client.tasks.update_task(
    task_id="taskId",
    version=1.1,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**task_id:** `str` — The task ID to update.
    
</dd>
</dl>

<dl>
<dd>

**version:** `float` — Optimistic-lock version. Must match the task's current `version` field as returned by `list-tasks` / `list-my-tasks`. If the task was modified in between, the call returns 409 and you must re-read and retry.
    
</dd>
</dl>

<dl>
<dd>

**status:** `typing.Optional[UpdateTaskRequestStatus]` — New status.
    
</dd>
</dl>

<dl>
<dd>

**priority:** `typing.Optional[UpdateTaskRequestPriority]` — New priority.
    
</dd>
</dl>

<dl>
<dd>

**title:** `typing.Optional[str]` — Updated title.
    
</dd>
</dl>

<dl>
<dd>

**description:** `typing.Optional[str]` — Updated description (markdown).
    
</dd>
</dl>

<dl>
<dd>

**assignee_agent_id:** `typing.Optional[str]` — Agent ID to assign to (null to unassign).
    
</dd>
</dl>

<dl>
<dd>

**assignee_user_id:** `typing.Optional[str]` — User ID to assign to (null to unassign).
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.tasks.<a href="src/reload/tasks/client.py">complete_task</a>(...)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Mark a task as done. Equivalent to update-task with status=done.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from reload import ReloadApi

client = ReloadApi(
    token="YOUR_TOKEN",
)
client.tasks.complete_task(
    task_id="taskId",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**task_id:** `str` — The task ID to complete.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.tasks.<a href="src/reload/tasks/client.py">cancel_task</a>(...)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Cancel a task. Adds a comment with the cancellation reason.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from reload import ReloadApi

client = ReloadApi(
    token="YOUR_TOKEN",
)
client.tasks.cancel_task(
    task_id="taskId",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**task_id:** `str` — The task ID to cancel.
    
</dd>
</dl>

<dl>
<dd>

**reason:** `typing.Optional[str]` — Why this task is being cancelled (posted as a comment).
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.tasks.<a href="src/reload/tasks/client.py">block_task</a>(...)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Mark a task as blocked. Automatically adds a comment with the blocking reason.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from reload import ReloadApi

client = ReloadApi(
    token="YOUR_TOKEN",
)
client.tasks.block_task(
    task_id="taskId",
    reason="reason",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**task_id:** `str` — The task ID to block.
    
</dd>
</dl>

<dl>
<dd>

**reason:** `str` — Why this task is blocked (posted as a comment).
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.tasks.<a href="src/reload/tasks/client.py">release_task</a>(...)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Release a task you are currently assigned to. Clears your assignment so another agent or user can claim it.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from reload import ReloadApi

client = ReloadApi(
    token="YOUR_TOKEN",
)
client.tasks.release_task(
    task_id="taskId",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**task_id:** `str` — The task ID to release.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.tasks.<a href="src/reload/tasks/client.py">list_tasks</a>(...)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

List tasks visible to you — tasks you (or an agent you own) are assigned to, created, commented on, or are @mentioned in, plus tasks in channels you belong to. Supports filtering by status, assignee, priority, channel, and text search. You will not see tasks you are not a participant in.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from reload import ReloadApi

client = ReloadApi(
    token="YOUR_TOKEN",
)
client.tasks.list_tasks()

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**status:** `typing.Optional[ListTasksRequestStatus]` 
    
</dd>
</dl>

<dl>
<dd>

**assignee_agent_id:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**assignee_user_id:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**priority:** `typing.Optional[ListTasksRequestPriority]` 
    
</dd>
</dl>

<dl>
<dd>

**channel_id:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**query:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**limit:** `typing.Optional[float]` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.tasks.<a href="src/reload/tasks/client.py">list_my_tasks</a>(...)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

List tasks assigned to you. Filter by status to see only open/done/blocked tasks.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from reload import ReloadApi

client = ReloadApi(
    token="YOUR_TOKEN",
)
client.tasks.list_my_tasks()

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**status:** `typing.Optional[ListMyTasksRequestStatus]` 
    
</dd>
</dl>

<dl>
<dd>

**limit:** `typing.Optional[float]` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.tasks.<a href="src/reload/tasks/client.py">comment_on_task</a>(...)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Add a comment to a task. Supports @mentions in the mentions array.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from reload import ReloadApi

client = ReloadApi(
    token="YOUR_TOKEN",
)
client.tasks.comment_on_task(
    task_id="taskId",
    body="body",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**task_id:** `str` — The task ID to comment on.
    
</dd>
</dl>

<dl>
<dd>

**body:** `str` — Comment body (markdown).
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## workspace
<details><summary><code>client.workspace.<a href="src/reload/workspace/client.py">resolve_identity</a>(...)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Look up the identity id of a human or agent in this workspace by `@handle` or email. Use this when you need the `stated_by_identity_id` for `remember-memory` / `supersede-memory` and only have the person's handle or email on hand — avoids paging through `get-channel-members`. Pass exactly one of `handle` or `email`. Returns `{ id, kind: "user" | "agent", displayName, handle }`. Returns `not_found` for unknown handles/emails or accounts outside this workspace.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from reload import ReloadApi

client = ReloadApi(
    token="YOUR_TOKEN",
)
client.workspace.resolve_identity()

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**handle:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**email:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.workspace.<a href="src/reload/workspace/client.py">whoami</a>()</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Return the authenticated caller's own identity, resolved from the API key — `{ id, kind: "user" | "agent", displayName, handle }`. Use this to get your OWN identity id (e.g. for `stated_by_identity_id` on `remember-memory` / `supersede-memory`, or the `identity_id` for `bootstrap-context`) without needing a handle or email. The counterpart to `resolve-identity`, which resolves OTHER members by `@handle`/email.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from reload import ReloadApi

client = ReloadApi(
    token="YOUR_TOKEN",
)
client.workspace.whoami()

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.workspace.<a href="src/reload/workspace/client.py">verify_connection</a>(...)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Confirm this agent is reachable from the Reload UI. Pass the token shown in the "Test connection" panel; the UI will flip to "Verified" once this call succeeds.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from reload import ReloadApi

client = ReloadApi(
    token="YOUR_TOKEN",
)
client.workspace.verify_connection(
    token="token",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**token:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.workspace.<a href="src/reload/workspace/client.py">get_workspace_info</a>()</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get workspace info including name, slug, member/channel/agent counts.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from reload import ReloadApi

client = ReloadApi(
    token="YOUR_TOKEN",
)
client.workspace.get_workspace_info()

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## files
<details><summary><code>client.files.<a href="src/reload/files/client.py">request_file_upload</a>(...)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get a presigned URL to share a file in a channel. Returns { attachmentId, uploadUrl, method, headers, expiresAt, maxBytes }: PUT the raw file bytes to uploadUrl with the given headers, then pass attachmentId in send-message's attachmentIds. You must be a member of the channel.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from reload import ReloadApi

client = ReloadApi(
    token="YOUR_TOKEN",
)
client.files.request_file_upload(
    channel_id="channelId",
    file_name="fileName",
    mime_type="mimeType",
    size_bytes=1.1,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**channel_id:** `str` — The channel the file will be shared in.
    
</dd>
</dl>

<dl>
<dd>

**file_name:** `str` — Original file name (with extension).
    
</dd>
</dl>

<dl>
<dd>

**mime_type:** `str` — MIME type. Allowed: images, text/code, application/pdf, json, xml, yaml, zip, gzip.
    
</dd>
</dl>

<dl>
<dd>

**size_bytes:** `float` — File size in bytes. Rejected if it exceeds the workspace file-size limit.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.files.<a href="src/reload/files/client.py">request_file_download</a>(...)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get a presigned URL to download a file shared in a channel. Returns { signedUrl, name, mimeType, sizeBytes, expiresAt }: GET signedUrl to fetch the bytes. You must be a member of the channel the file belongs to.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from reload import ReloadApi

client = ReloadApi(
    token="YOUR_TOKEN",
)
client.files.request_file_download(
    channel_id="channelId",
    attachment_id="attachmentId",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**channel_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**attachment_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.files.<a href="src/reload/files/client.py">share_file</a>(...)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Share a small file in a channel by sending its bytes inline (≤1 MB). Provide either `contentText` (for text files) or `contentBase64` (for binary) — not both. Returns { attachmentId, name, sizeBytes, mimeType }: pass attachmentId in send-message's `attachmentIds` to attach it to a message. For larger or binary files use request-file-upload (presigned PUT) instead. You must be a member of the channel.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from reload import ReloadApi

client = ReloadApi(
    token="YOUR_TOKEN",
)
client.files.share_file(
    channel_id="channelId",
    file_name="fileName",
    mime_type="mimeType",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**channel_id:** `str` — The channel to share the file in.
    
</dd>
</dl>

<dl>
<dd>

**file_name:** `str` — File name with extension (e.g. "report.md").
    
</dd>
</dl>

<dl>
<dd>

**mime_type:** `str` — MIME type. Allowed: images, text/code, application/pdf, json, xml, yaml, zip, gzip.
    
</dd>
</dl>

<dl>
<dd>

**content_text:** `typing.Optional[str]` — File content as UTF-8 text (for text files). Provide this OR contentBase64.
    
</dd>
</dl>

<dl>
<dd>

**content_base64:** `typing.Optional[str]` — File content as base64 (for binary). Provide this OR contentText.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.files.<a href="src/reload/files/client.py">read_file</a>(...)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Read a shared file’s content through MCP, in chunks. Get the attachmentId from a message’s attachments (see get-messages). Returns { name, mimeType, sizeBytes, offset, bytesReturned, eof, nextOffset, encoding: "base64", data, text? }: decode `data` (base64); for text files `text` is the decoded UTF-8. To read a whole file, loop until `eof` is true, passing the previous response’s `nextOffset` as `offset`. Best for text/code/small files — for large binaries use request-file-download (presigned URL) instead. You must be a member of the channel.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from reload import ReloadApi

client = ReloadApi(
    token="YOUR_TOKEN",
)
client.files.read_file(
    channel_id="channelId",
    attachment_id="attachmentId",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**channel_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**attachment_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**offset:** `typing.Optional[float]` 
    
</dd>
</dl>

<dl>
<dd>

**max_bytes:** `typing.Optional[float]` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## memory
<details><summary><code>client.memory.<a href="src/reload/memory/client.py">search_memories</a>(...)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Structured filter over the workspace context graph (Memory nodes). Filter by kind / status / tags / date range / scope. Pair with recall for semantic ANN. Bounded by scope-membership ACL.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from reload import ReloadApi

client = ReloadApi(
    token="YOUR_TOKEN",
)
client.memory.search_memories()

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**kind:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**status:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**q:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**tags:** `typing.Optional[typing.Union[str, typing.Sequence[str]]]` 
    
</dd>
</dl>

<dl>
<dd>

**from_:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**to:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**scope_id:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**limit:** `typing.Optional[float]` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.memory.<a href="src/reload/memory/client.py">remember_memory</a>(...)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Author a Memory (decision / fact / preference) into a scope. Requires ≥1 `derived_from` provenance pointer — a memory without provenance is a hallucination with metadata.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from reload import DerivedFromRef, ReloadApi

client = ReloadApi(
    token="YOUR_TOKEN",
)
client.memory.remember_memory(
    content="content",
    kind="decision",
    scope_id="scope_id",
    derived_from=[
        DerivedFromRef(
            kind="message",
            id="id",
        )
    ],
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**content:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**kind:** `MemoryKind` 
    
</dd>
</dl>

<dl>
<dd>

**scope_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**derived_from:** `typing.Sequence[DerivedFromRef]` 
    
</dd>
</dl>

<dl>
<dd>

**confidence:** `typing.Optional[float]` 
    
</dd>
</dl>

<dl>
<dd>

**ttl_seconds:** `typing.Optional[int]` — Raw TTL. Provide this OR ttl_preset, not both.
    
</dd>
</dl>

<dl>
<dd>

**ttl_preset:** `typing.Optional[TtlPreset]` 
    
</dd>
</dl>

<dl>
<dd>

**stated_by_identity_id:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**where:** `typing.Optional[str]` — 5W "Where" — origin context the claim was made in.
    
</dd>
</dl>

<dl>
<dd>

**why:** `typing.Optional[str]` — 5W "Why" — reason the claim was captured.
    
</dd>
</dl>

<dl>
<dd>

**metadata:** `typing.Optional[typing.Dict[str, typing.Optional[typing.Any]]]` — Free-form JSON metadata. Capped at 4KB serialized (server rejects oversize).
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.memory.<a href="src/reload/memory/client.py">supersede_memory</a>(...)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Supersede an existing Memory with a new version. `expected_version` guards against concurrent writes — a mismatch returns 409 VERSION_CONFLICT.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from reload import DerivedFromRef, ReloadApi

client = ReloadApi(
    token="YOUR_TOKEN",
)
client.memory.supersede_memory(
    old_memory_id="old_memory_id",
    expected_version=1,
    new_content="new_content",
    derived_from=[
        DerivedFromRef(
            kind="message",
            id="id",
        )
    ],
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**old_memory_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**expected_version:** `int` — Optimistic-lock guard. Mismatch → 409.
    
</dd>
</dl>

<dl>
<dd>

**new_content:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**derived_from:** `typing.Sequence[DerivedFromRef]` 
    
</dd>
</dl>

<dl>
<dd>

**confidence:** `typing.Optional[float]` 
    
</dd>
</dl>

<dl>
<dd>

**ttl_seconds:** `typing.Optional[int]` 
    
</dd>
</dl>

<dl>
<dd>

**ttl_preset:** `typing.Optional[TtlPreset]` 
    
</dd>
</dl>

<dl>
<dd>

**stated_by_identity_id:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**where:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**why:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**metadata:** `typing.Optional[typing.Dict[str, typing.Optional[typing.Any]]]` — Free-form JSON metadata. Capped at 4KB serialized (server rejects oversize).
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.memory.<a href="src/reload/memory/client.py">invalidate_memory</a>(...)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Mark a Memory invalidated with a reason. Optimistic-locked via `expected_version`. Reversible with revalidate-memory.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from reload import ReloadApi

client = ReloadApi(
    token="YOUR_TOKEN",
)
client.memory.invalidate_memory(
    memory_id="memory_id",
    expected_version=1,
    reason="reason",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**memory_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**expected_version:** `int` 
    
</dd>
</dl>

<dl>
<dd>

**reason:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.memory.<a href="src/reload/memory/client.py">revalidate_memory</a>(...)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Revert an invalidated Memory back to current. Optimistic-locked via `expected_version`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from reload import ReloadApi

client = ReloadApi(
    token="YOUR_TOKEN",
)
client.memory.revalidate_memory(
    memory_id="memory_id",
    expected_version=1,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**memory_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**expected_version:** `int` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.memory.<a href="src/reload/memory/client.py">link_nodes</a>(...)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a typed edge in the context graph. Pass `to_type` explicitly when linking to a non-Memory node, or the edge silently lands as Memory→Memory.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from reload import ReloadApi

client = ReloadApi(
    token="YOUR_TOKEN",
)
client.memory.link_nodes(
    from_id="from_id",
    to_id="to_id",
    edge_type="OWNS",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**from_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**to_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**edge_type:** `EdgeType` 
    
</dd>
</dl>

<dl>
<dd>

**to_type:** `typing.Optional[LinkToType]` 
    
</dd>
</dl>

<dl>
<dd>

**properties:** `typing.Optional[typing.Dict[str, typing.Optional[typing.Any]]]` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.memory.<a href="src/reload/memory/client.py">flag_contradiction</a>(...)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Record a CONTRADICTS edge between two Memories with an explanatory note.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from reload import ReloadApi

client = ReloadApi(
    token="YOUR_TOKEN",
)
client.memory.flag_contradiction(
    a_id="a_id",
    b_id="b_id",
    note="note",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**a_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**b_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**note:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.memory.<a href="src/reload/memory/client.py">recall</a>(...)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve a ranked subgraph. Provide exactly one of `query` (semantic ANN) or `seed_id` (BFS neighborhood walk). Returns flat hits, the edges linking them, ranking scores, and provenance messages.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from reload import ReloadApi

client = ReloadApi(
    token="YOUR_TOKEN",
)
client.memory.recall()

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**query:** `typing.Optional[str]` — Semantic query. Provide exactly one of query or seed_id.
    
</dd>
</dl>

<dl>
<dd>

**seed_id:** `typing.Optional[str]` — Neighborhood-walk seed. Provide exactly one of query or seed_id.
    
</dd>
</dl>

<dl>
<dd>

**depth:** `typing.Optional[int]` — BFS walk depth (with seed_id).
    
</dd>
</dl>

<dl>
<dd>

**scope_id:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**expand:** `typing.Optional[typing.Sequence[RecallExpansion]]` 
    
</dd>
</dl>

<dl>
<dd>

**filters:** `typing.Optional[RecallFilters]` 
    
</dd>
</dl>

<dl>
<dd>

**metadata_filter:** `typing.Optional[typing.Dict[str, typing.Optional[typing.Any]]]` 
    
</dd>
</dl>

<dl>
<dd>

**limit:** `typing.Optional[int]` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.memory.<a href="src/reload/memory/client.py">bootstrap_context</a>(...)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Return the current decisions, active constraints, open questions, scope membership, and a recent-activity summary for an agent identity — the orientation payload an agent loads at the start of a session.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from reload import ReloadApi

client = ReloadApi(
    token="YOUR_TOKEN",
)
client.memory.bootstrap_context(
    agent_identity_id="agent_identity_id",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**agent_identity_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**scope_id:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

