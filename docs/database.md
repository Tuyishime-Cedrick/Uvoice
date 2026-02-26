# Database (Draft)

## User
- id
- email
- password_hash
- created_at

## Debate
- id
- title
- description
- created_by (FK User)
- created_at

## Argument
- id
- debate_id (FK Debate)
- author_id (FK User, optional for MVP)
- type (FOR/AGAINST)
- content
- created_at

## Vote
- id
- user_id (FK User, optional for MVP)
- argument_id (FK Argument)
- value (+1)
- UNIQUE(user_id, argument_id) when auth exists
