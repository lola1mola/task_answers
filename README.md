# Answers - task 3

## All
[Ссылка на скринкаст дз](https://drive.google.com/file/d/1SRHsX0N8va1BYFhgy_wm_pDgz42vuGH6/view?usp=sharing)

## SQL
``` SELECT users.username FROM users ```
``` SELECT users.username, count(*) as received_messages FROM users inner join messages on users.id = messages.to_id GROUP BY users.username ORDER BY received_messages DESC LIMIT 1 ```
``` SELECT users.username, count(*) as sent_messages FROM users inner join messages on users.id = messages.from_id GROUP BY users.username ```
``` SELECT users.username, (COUNT(messages.id)/COUNT(DISTINCT from_id)) as avg FROM users inner join messages on users.id = messages.from_id GROUP BY users.username ```


