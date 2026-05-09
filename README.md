# NITC Curriculum Data

Institution data repository for **National Institute of Technology Calicut (NITC)** — the data source for the [Changala](https://changala.app) ring.

## Structure

```
nitc-curriculum-data/
├── meta.json                         # Institution metadata
├── calendar/
│   ├── 2025-2026.json                     # Academic calendar
│   └── holidays.json                      # Standing holidays
├── institute-core/
│   └── courses.json                       # IC courses shared across all departments
├── departments/
│   ├── cse/                          # Computer Science and Engineering
│   ├── ece/                          # Electronics and Communication Engineering
│   ├── eee/                          # Electrical and Electronics Engineering
│   ├── me/                           # Mechanical Engineering
│   ├── ce/                           # Civil Engineering
│   └── che/                          # Chemical Engineering
│       ├── department.json           # Department info
│       ├── courses.json              # Course catalog
│       ├── electives.json            # Elective offerings
│       └── faculty.json              # Faculty directory
├── semesters/
│   └── 2025-monsoon/
│       ├── semester.json             # Semester metadata
│       ├── offerings.json            # Courses offered this semester
│       └── timetable/
│           └── slots.json            # Slot definitions
└── README.md
```

## How This Repo Is Used

This repository is the **reference data layer** for the NITC Changala ring. It is consumed by the MCP server to bootstrap courses, sessions, and enrollments into the ring.

1. Curriculum PDFs are parsed to JSON and committed here
2. An admin uses MCP (via AI assistant) to load data into the ring
3. The ring stores runtime state (active courses, sessions, enrollments)
4. This repo preserves the canonical academic structure across semesters

## Contributing

- Anyone can propose changes via PR
- Department volunteers and class representatives maintain accuracy
- Changes are reviewed before being loaded into the ring

## License

See [LICENSE](LICENSE) for details.
