# collaborative-editor/
├── README.md                    # Architecture + how to run + demo video link
├── docs/
│   ├── architecture.md          # Detailed design (C4 style)
│   ├── crdt-explanation.md      # Why CRDT > OT for this use case
│   └── scaling.md               # How to scale the WebSocket layer
├── packages/
│   ├── client/                  # React + Yjs frontend
│   │   ├── src/
│   │   │   ├── components/
│   │   │   │   ├── Editor.tsx
│   │   │   │   ├── Presence.tsx
│   │   │   │   └── Status.tsx
│   │   │   ├── hooks/
│   │   │   │   └── useYjs.ts
│   │   │   └── providers/
│   │   │       └── CustomWebsocketProvider.ts
│   │   └── package.json
│   └── server/                  # Custom WebSocket sync server
│       ├── src/
│       │   ├── server.ts
│       │   ├── room.ts
│       │   ├── yjs-handler.ts
│       │   └── redis.ts         # optional multi-instance
│       └── package.json
├── docker-compose.yml
└── .github/workflows/ci.yml-