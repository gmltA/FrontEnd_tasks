## Table of Contents

- [Task description](#Task-description)
- [Variations](#Variations)
  - [One](#One)
  - [Two](#Two)
  - [Three](#Three)
  - [Four](#Four)

# Task description

Create a console messaging application. No separate client / server applications are allowed. After the launch, client can choose the display name. This name will be used later to identify the sender of the message. Message exchange to be performed via manual socket management. You can use any programming language of your choice.


# Variations

## One
Initial connection via TCP, message exchange via UDP. Only one to one connection is supported.

Message order control. Each message should contain order-related parameter, so that receiving client could display messages in the right order.

## Two
Initial connection and message exchange via UDP. Only one to one connection is supported.

Each client stores message history. If the same client connects after a disconnect, messages have to be recovered and displayed by reconnected client. To distinguish between clients, an unique identifier should be generated for each client.

## Three
Initial connection and message exchange via UDP. Only one to one connection is supported.

Message order control. Each message should contain order-related parameter, so that receiving client could display messages in the right order. Both clients should somehow control that no messages were lost on their way to receiver.

## Four
Group message exchange via UDP (see multicast and broadcast).

Any client can create a group with unique identifier. Other clients can request an access to the group by identifier. Group creator listents to such invites and can allow or deny access for a specific client. Only after group creator allowed access, corresponding client will receive group messages.
