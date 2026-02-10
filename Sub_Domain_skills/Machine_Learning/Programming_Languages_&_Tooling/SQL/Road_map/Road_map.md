# 🗄️ SQL DATABASE MASTER ROADMAP (MOST EXHAUSTIVE)
# Scope: SQL + Relational database concepts + production DBA/dev skills (vendor-neutral + major vendor specifics)
# Format rule: ONLY "-" with indentation (deep tree)

=====================================================================
CORE FOUNDATIONS (what a SQL database is)
=====================================================================

- Database purpose
  - persistent storage
    - durability goals
  - multi-user access
    - concurrency goals
  - correctness guarantees
    - consistency goals

- Relational model (the “math” behind SQL)
  - relation (table)
    - tuple (row)
      - attribute (column)
  - keys
    - candidate key
      - primary key
        - surrogate vs natural key
    - alternate keys
    - foreign key
      - referential integrity
  - relationships
    - one-to-one
    - one-to-many
    - many-to-many
      - junction table
  - NULL semantics
    - unknown vs missing vs not applicable
      - three-valued logic in SQL

- Transaction model
  - ACID
    - atomicity
    - consistency
    - isolation
    - durability
  - transaction boundaries
    - autocommit
    - explicit BEGIN/COMMIT/ROLLBACK
  - isolation levels (standard concept)
    - read uncommitted
    - read committed
    - repeatable read
    - serializable
  - anomalies
    - dirty read
    - non-repeatable read
    - phantom read

- Workload types
  - OLTP (transactions)
    - many small reads/writes
      - strict latency
  - OLAP (analytics)
    - large scans/aggregations
      - throughput focus
  - HTAP (mixed)
    - hybrid tradeoffs

=====================================================================
SQL LANGUAGE OVERVIEW (what to learn as “SQL”)
=====================================================================

- SQL categories (command families)
  - DDL (schema definition)
    - CREATE
    - ALTER
    - DROP
    - TRUNCATE
  - DML (data manipulation)
    - INSERT
    - UPDATE
    - DELETE
    - MERGE / UPSERT (vendor dependent)
  - DQL (querying)
    - SELECT
  - TCL (transaction control)
    - BEGIN / START TRANSACTION
    - COMMIT
    - ROLLBACK
    - SAVEPOINT
    - SET TRANSACTION ISOLATION LEVEL
  - DCL (access control)
    - GRANT
    - REVOKE

=====================================================================
SCHEMA DESIGN (data modeling)
=====================================================================

- Requirements → model
  - entities
    - attributes
      - domain types
  - relationships
    - cardinality
      - optionality
  - constraints as rules
    - must be enforced in DB when possible

- Normalization (design correctness)
  - functional dependencies
  - normal forms
    - 1NF
      - atomic values
    - 2NF
      - no partial dependency on composite key
    - 3NF
      - no transitive dependency
    - BCNF (advanced)
  - denormalization (performance-driven)
    - when justified
    - how to keep consistent (jobs/triggers/materialized views)

- Data types (portable concepts)
  - numeric
    - integer sizes
    - decimal/numeric (exact)
    - float/double (approx)
  - text
    - char/varchar/text
    - collation and case rules
  - date/time
    - date
    - time
    - timestamp
    - timezone handling (vendor differences)
  - boolean
  - binary
    - blob/bytea
  - UUID
  - JSON (semi-structured, vendor dependent)
  - arrays (vendor dependent)
  - enums (vendor dependent)

- Naming conventions
  - table/column naming consistency
  - singular vs plural rule
  - avoid reserved keywords
  - consistent PK/FK naming

=====================================================================
DDL (CREATE / ALTER / DROP) — DEEP
=====================================================================

- Databases and schemas/namespaces (vendor dependent naming)
  - create database
    - encoding/collation defaults
  - create schema / namespace
    - ownership
    - search path (vendor dependent)

- Tables
  - CREATE TABLE essentials
    - column definitions
      - type
      - nullability
      - default
    - constraints
      - PRIMARY KEY
      - FOREIGN KEY
      - UNIQUE
      - CHECK
      - NOT NULL
    - computed/generated columns (vendor dependent)
    - identity/auto-increment (vendor dependent)
  - ALTER TABLE
    - add column
    - drop column
    - change type (risk)
    - add/drop constraints
    - rename table/column
  - TRUNCATE vs DELETE
    - transactional behavior varies
    - FK restrictions

- Indexes (DDL object)
  - CREATE INDEX
    - single-column
    - multi-column (composite)
      - column order importance
    - unique index
    - partial/filtered index (vendor dependent)
    - expression/function index (vendor dependent)
    - covering/included columns (vendor dependent)
  - DROP/REINDEX

- Views
  - CREATE VIEW
    - security/abstraction layer
  - updatable views (limits)
  - materialized views (vendor dependent)
    - refresh strategy

- Constraints (deeper)
  - PK
    - clustered vs non-clustered (vendor dependent)
  - FK
    - ON DELETE
      - CASCADE
      - SET NULL
      - RESTRICT/NO ACTION
    - ON UPDATE behavior
  - UNIQUE
    - multiple unique constraints
  - CHECK
    - domain rules
  - DEFERRABLE constraints (vendor dependent)
    - deferrable FK checks

=====================================================================
DML (INSERT / UPDATE / DELETE) — DEEP
=====================================================================

- INSERT
  - single row insert
  - multi-row insert
  - INSERT ... SELECT
  - default values
  - returning inserted values (vendor dependent)
  - upsert patterns
    - ON CONFLICT DO UPDATE (Postgres)
    - INSERT ... ON DUPLICATE KEY UPDATE (MySQL)
    - MERGE (SQL Server/Oracle/others)

- UPDATE
  - update with where clause
  - update with joins (vendor dependent syntax)
  - update from subquery/CTE
  - returning updated values (vendor dependent)
  - safe updates
    - always test with SELECT first

- DELETE
  - delete with where clause
  - delete with joins (vendor dependent)
  - cascading deletes via FK rules
  - soft delete pattern
    - deleted_at flag
    - partial unique constraints (vendor dependent)
  - purge strategy
    - partition drop strategy (advanced)

=====================================================================
SELECT (QUERIES) — THE BIGGEST PART
=====================================================================

- Query shape
  - SELECT list
    - columns
    - expressions
    - aliases
    - DISTINCT
  - FROM
    - tables
    - subqueries
    - CTE references
  - WHERE
    - predicates
      - comparison
      - LIKE / ILIKE (vendor dependent)
      - IN
      - BETWEEN
      - EXISTS
      - NULL checks
        - IS NULL / IS NOT NULL
    - boolean logic
      - AND/OR/NOT
      - parentheses precedence
  - GROUP BY
    - grouping keys
    - aggregate functions
  - HAVING
    - filtering groups
  - ORDER BY
    - sort keys
    - NULLS FIRST/LAST (vendor dependent)
  - LIMIT/OFFSET
    - pagination
      - offset pagination drawbacks
      - keyset/cursor pagination strategy

- Joins (deep)
  - inner join
  - left outer join
  - right outer join
  - full outer join (vendor dependent support)
  - cross join
  - join conditions
    - equi-join
    - non-equi join
  - self join patterns
  - anti-join patterns
    - NOT EXISTS
    - LEFT JOIN ... IS NULL
  - semi-join patterns
    - EXISTS
  - join performance concepts
    - cardinality
    - join order
    - selective predicates early

- Subqueries (deep)
  - scalar subquery
  - inline view (derived table)
  - correlated subquery
  - EXISTS / NOT EXISTS
  - ANY / ALL (vendor dependent nuances)

- CTEs (WITH)
  - single CTE
  - multiple CTEs in one query (comma-separated) :contentReference[oaicite:0]{index=0}
  - CTE as readability tool
  - CTE optimization notes (vendor dependent)
  - recursive CTE (advanced)
    - hierarchical data
    - graph traversal (limited)

- Set operations
  - UNION
    - UNION ALL
  - INTERSECT (vendor dependent)
  - EXCEPT / MINUS (vendor dependent)
  - set semantics vs bag semantics

- Window functions (advanced querying)
  - OVER() clause
    - PARTITION BY
    - ORDER BY
    - frame clauses
      - ROWS
      - RANGE
      - BETWEEN ... AND ...
  - ranking
    - ROW_NUMBER
    - RANK
    - DENSE_RANK
    - NTILE
  - analytics
    - SUM/AVG over window
    - LAG/LEAD
    - FIRST_VALUE/LAST_VALUE
  - common patterns
    - top-N per group
    - running totals
    - sessionization (advanced)

- Aggregations (deep)
  - COUNT(*), COUNT(col)
  - SUM/AVG/MIN/MAX
  - GROUPING SETS / ROLLUP / CUBE (vendor dependent)
  - distinct aggregation
    - COUNT(DISTINCT x)
  - filtered aggregates (vendor dependent)

- Functions (broad categories)
  - numeric functions
  - string functions
    - trim/replace/substr/concat
  - date/time functions
    - date truncation
    - intervals (vendor dependent)
  - null-handling functions
    - COALESCE
    - NULLIF
  - conditional expressions
    - CASE WHEN THEN ELSE END
  - type conversion
    - CAST
    - vendor-specific convert functions
  - JSON functions (vendor dependent)
    - extraction
    - indexing strategies

=====================================================================
TRANSACTIONS + CONCURRENCY (PRODUCTION-CRITICAL)
=====================================================================

- Transaction control (TCL)
  - autocommit vs explicit transactions
  - BEGIN/START TRANSACTION
  - COMMIT
  - ROLLBACK
  - SAVEPOINT
    - rollback to savepoint
  - SET TRANSACTION properties
    - isolation level
    - read-only (vendor dependent)

- Isolation levels (standard + vendor reality)
  - standard four levels (SQL:1992)
    - read uncommitted
    - read committed
    - repeatable read
    - serializable
  - MySQL InnoDB supports all four; default is REPEATABLE READ :contentReference[oaicite:1]{index=1}
  - PostgreSQL maps READ UNCOMMITTED to READ COMMITTED (MVCC reality) :contentReference[oaicite:2]{index=2}

- Locking & MVCC (concepts)
  - locking types
    - row locks
    - table locks
    - metadata/schema locks
  - MVCC (multi-version concurrency control)
    - snapshots
    - visibility rules
  - anomalies & behavior mapping
    - phantom reads
    - write skew (advanced)
  - deadlocks
    - how they happen
    - detection
    - retry strategy
  - long transactions
    - why they hurt
    - how to avoid

=====================================================================
INDEXING (MAKE QUERIES FAST)
=====================================================================

- Why indexes exist
  - avoid full table scans
  - accelerate lookups, joins, sorting

- Index basics
  - B-tree index concept
  - index selectivity
  - composite indexes
    - leftmost-prefix rule (common)
    - column order strategy
  - covering indexes
    - index-only scans concept
  - unique indexes vs constraints
  - partial/filtered indexes (vendor dependent)
  - expression/function indexes (vendor dependent)

- Choosing indexes
  - for WHERE filters
  - for JOIN keys
  - for ORDER BY
  - for GROUP BY
  - for uniqueness enforcement

- Index pitfalls
  - too many indexes slow writes
  - low-selectivity indexes (e.g., boolean) often useless
  - stale statistics cause bad plans

=====================================================================
QUERY OPTIMIZATION (EXPLAIN + PLANNER THINKING)
=====================================================================

- Query planning
  - logical plan vs physical plan
  - cost-based optimization
  - statistics
    - table stats
    - column distribution
    - histograms (vendor dependent)

- EXPLAIN usage
  - read plan nodes
  - identify
    - sequential scan vs index scan
    - hash join vs merge join vs nested loop join
    - sort operations
    - aggregation strategies

- Optimization techniques (portable)
  - reduce rows early (filter first)
  - avoid SELECT *
  - avoid functions on indexed columns in WHERE (unless expression index)
  - replace correlated subqueries with joins/CTEs when beneficial
  - fix N+1 query patterns at app layer (concept)
  - use keyset pagination instead of OFFSET for big datasets
  - precompute heavy aggregates (materialized views / summary tables)

=====================================================================
VIEWS, PROCEDURES, TRIGGERS (DB-SIDE PROGRAMMING)
=====================================================================

- Views
  - abstraction layer
  - permissions boundary (sometimes)
  - performance notes (depends on optimizer)

- Stored procedures / functions (vendor dependent)
  - when to use
    - complex server-side logic
    - reducing network chatter
  - risks
    - portability
    - versioning complexity

- Triggers
  - BEFORE/AFTER triggers
  - use cases
    - audit logging
    - denormalization maintenance
  - risks
    - hidden side effects
    - debugging difficulty

=====================================================================
SECURITY (SQL DATABASE)
=====================================================================

- Authentication vs authorization
  - users/logins
  - roles/groups

- Permissions (DCL)
  - GRANT
    - table privileges
      - SELECT
      - INSERT
      - UPDATE
      - DELETE
    - schema/database privileges
  - REVOKE
  - least privilege principle
    - separate app user vs admin user

- SQL injection awareness (SQL-side + app-side)
  - principle
    - never treat user input as SQL code
  - prepared statements concept (implementation varies)
  - escaping is not enough in general

- Encryption
  - TLS connections to DB (transport encryption)
  - at-rest encryption (storage encryption, vendor/cloud dependent)

- Auditing (advanced)
  - statement logging
  - access logs
  - privileged action tracking

=====================================================================
BACKUPS, RECOVERY, OPERATIONS (DBA SKILLS)
=====================================================================

- Backups
  - logical backups
    - dump schema/data
  - physical backups
    - file-level/snapshot
  - backup verification
    - restore drills

- Recovery
  - point-in-time recovery concept (PITR)
  - restore ordering
    - schema then data then constraints (sometimes)

- Maintenance
  - statistics updates
  - vacuum/cleanup (vendor dependent)
  - index maintenance/rebuild (vendor dependent)

=====================================================================
SCALING (BIGGER THAN ONE MACHINE)
=====================================================================

- Vertical scaling
  - CPU/RAM/IO improvements

- Replication
  - primary-replica
    - read scaling
    - failover concept
  - replication lag
    - consistency tradeoffs

- Sharding (advanced)
  - partition key selection
  - routing layer complexity

- Partitioning (table-level)
  - range partitioning (time-based)
  - hash partitioning
  - partition pruning
  - maintenance benefits (drop old partitions fast)

- High availability (HA)
  - failover automation concept
  - split-brain prevention concept
  - monitoring + health checks

=====================================================================
DATA WAREHOUSING (SQL FOR ANALYTICS)
=====================================================================

- Dimensional modeling (OLAP)
  - fact tables
  - dimension tables
  - star schema
  - snowflake schema
  - slowly changing dimensions (SCD concept)

- ETL/ELT concepts
  - staging tables
  - incremental loads
  - deduplication
  - late-arriving data

- Analytical SQL patterns
  - window functions heavy usage
  - rollups/cubes (if supported)
  - approximate aggregation (vendor dependent)

=====================================================================
VENDOR-SPECIFIC TRACKS (OPTIONAL, BUT “COMPLETE” IN REAL LIFE)
=====================================================================

- PostgreSQL track
  - MVCC behavior & isolation mapping :contentReference[oaicite:3]{index=3}
  - EXPLAIN (ANALYZE)
  - VACUUM concepts
  - JSONB + GIN indexing
  - extensions (PostGIS, etc.)

- MySQL/InnoDB track
  - isolation levels and defaults :contentReference[oaicite:4]{index=4}
  - EXPLAIN format differences
  - InnoDB engine behavior

- SQL Server track (optional)
  - T-SQL differences
  - clustered indexes behavior
  - execution plan tooling

- Oracle track (optional)
  - PL/SQL differences
  - optimizer statistics

=====================================================================
“SQL COMPLETE” CHECKLIST (END STATE)
=====================================================================

- You can design schemas with constraints + indexes
- You can write complex queries
  - joins
  - subqueries
  - CTEs
  - window functions
- You can reason about transactions + isolation + locking
  - and explain anomalies and fixes
- You can optimize slow queries with EXPLAIN and indexing strategy
- You can operate a database safely
  - backups
  - restore drills
  - permissions
  - replication/partitioning concepts

