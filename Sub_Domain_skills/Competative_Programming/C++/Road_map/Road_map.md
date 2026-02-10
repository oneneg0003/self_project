# 🧠 C++ COMPLETE MASTER ROADMAP (ULTRA-EXHAUSTIVE)
# Format rule: ONLY dashes. Depth is shown by indentation only.

=====================================================================
FOUNDATIONS: TOOLCHAIN + HOW C++ BUILDS + HOW PROGRAMS RUN
=====================================================================

- What C++ is (practical view)
  - compiled, statically typed, multi-paradigm language
    - low-level control + high-level abstractions
      - performance-critical systems
        - large-scale software

- Translation pipeline (the real build stages)
  - preprocessing
    - header inclusion expansion
      - include search paths
        - system includes vs local includes
          - include guards vs pragma once
    - macro expansion
      - object-like macros
        - pitfalls: no types, no scope
          - prefer constexpr / inline / templates when possible
      - function-like macros
        - double evaluation hazards
          - prefer inline functions
      - conditional compilation
        - feature flags
          - platform flags
            - debug vs release toggles
  - compilation (per translation unit)
    - parsing to AST
      - syntax errors
        - semantic errors
          - name lookup
          - overload resolution
    - template instantiation
      - compile-time code generation
        - heavy compile-time cost
          - error messages become large
    - optimization passes
      - inlining decisions
        - constant propagation
          - dead code elimination
  - assembly generation
    - target ISA
      - calling conventions (ABI-level idea)
        - registers vs stack usage
  - linking
    - object files and libraries
      - static libraries (.a/.lib)
        - archive of objects
      - shared libraries (.so/.dll/.dylib)
        - runtime loading
    - symbol resolution
      - undefined reference errors
        - missing definitions
          - wrong link order
          - missing library in link step
      - ODR and multiple definitions
        - duplicate global symbols
          - header-only mistakes
  - loading and execution
    - program entry
      - crt startup
        - main invoked
    - runtime state
      - stack frames
        - return addresses
          - local variables lifetimes
      - heap allocations
        - allocator interaction
          - fragmentation considerations

- Choosing a C++ standard level
  - C++11/14/17/20/23 feature sets
    - what “modern C++” means
      - prefer RAII, move semantics, constexpr, templates used safely
        - keep portability goals
  - compiler feature support reality
    - feature availability varies by compiler/version
      - check compiler support tables when using newer features
        - especially for C++23 modules/ranges/format/print etc

- Compilers and platforms
  - GCC (g++)
    - warning levels and diagnostics
      - enabling strict warnings
        - treating warnings as errors
    - language mode selection
      - -std=c++20 / -std=c++23
        - gnu++ extensions vs strict ISO mode
  - Clang
    - similar front-end behavior
      - different diagnostics
        - excellent tooling ecosystem
  - MSVC
    - Windows toolchain patterns
      - MSBuild integration
        - ABI differences
  - cross-platform constraints
    - endianness
      - alignment
        - sizeof differences
          - pointer width differences

- Build systems (must-learn for real projects)
  - CMake (industry baseline)
    - configure vs build separation
      - out-of-source builds
        - build directory hygiene
    - targets model
      - add_library / add_executable
        - target_include_directories
        - target_link_libraries
      - usage requirements
        - PRIVATE/PUBLIC/INTERFACE
          - transitive include/link propagation
    - generator concept
      - Ninja generator
        - Visual Studio generator
          - Makefiles generator
    - presets
      - CMakePresets.json
        - reproducible configure/build
  - build types
    - Debug
      - symbols enabled
        - less optimization
    - Release
      - high optimization
        - stripped symbols
    - RelWithDebInfo
      - optimized + debug symbols
        - best for profiling/diagnosing

- Project layout conventions
  - src / include / tests / examples
    - public headers vs private headers
      - include hygiene
        - minimal includes
          - forward declarations when safe
  - single translation unit experiments
    - quick iteration
      - then scale to multi-file design

=====================================================================
C++ CORE LANGUAGE: SYNTAX → TYPES → EXPRESSIONS → STATEMENTS
=====================================================================

- Lexical basics
  - tokens and whitespace
    - comments
      - // single line
        - /* block */
    - identifiers and keywords
      - reserved names rules
        - leading underscore pitfalls
  - declarations vs definitions
    - declaration introduces name
      - definition allocates storage or provides body
        - difference drives linker errors

- Fundamental types
  - bool
    - truthiness rules
      - implicit conversions and pitfalls
  - character types
    - char, signed char, unsigned char
      - wchar_t, char16_t, char32_t
        - char8_t (UTF-8 code units)
  - integers
    - short, int, long, long long
      - signed/unsigned
        - overflow rules
          - signed overflow is UB
  - floating point
    - float, double, long double
      - precision and rounding
        - comparisons (epsilon)
  - void and nullptr
    - nullptr vs 0 vs NULL
      - overload resolution differences

- Literals
  - integer literals
    - bases (decimal/hex/oct/bin)
      - suffixes (u, l, ll)
  - floating literals
    - scientific notation
      - suffix f for float
  - character literals
    - escape sequences
      - u8/u/U prefixes
  - string literals
    - narrow and wide
      - raw string literals R"( ... )"
        - multiline patterns

- Operators and expressions
  - arithmetic
    - precedence and associativity
      - integer promotions
        - usual arithmetic conversions
  - comparisons
    - == != < <= > >=
      - three-way comparison (<=>) (modern)
  - boolean logic
    - short-circuit behavior
      - operator precedence with && and ||
  - bitwise operations
    - masks and flags
      - shifting rules
        - UB pitfalls (shift by width)
  - assignment
    - copy assignment
      - compound assignments
        - evaluation order considerations
  - increment/decrement
    - prefix vs postfix
      - performance and correctness
  - comma operator
    - rare usage
      - sequencing edge cases
  - conditional operator
    - ternary expression
      - type deduction rules
  - casts (critical)
    - implicit conversions
      - narrowing conversions
        - brace-init prevents narrowing
    - explicit casts
      - static_cast
        - safe-ish conversion
      - reinterpret_cast
        - bit-level reinterpretation
          - very dangerous
      - const_cast
        - remove constness
          - UB if modifying truly-const object
      - dynamic_cast
        - RTTI-based safe downcast
          - requires polymorphic base

- Statements and control flow
  - if / else
    - initialization in if (modern)
      - scope-limited variables
  - switch
    - fallthrough
      - [[fallthrough]] attribute
        - enum class patterns
  - loops
    - while
      - do-while
        - for
          - range-based for
            - structured bindings in loops
  - jump statements
    - break
      - continue
        - return
          - goto (avoid except special cases)
  - exceptions control flow
    - try/catch
      - stack unwinding

=====================================================================
OBJECT MODEL + LIFETIMES + MEMORY (THE MOST IMPORTANT PART)
=====================================================================

- Values, objects, and lifetimes
  - automatic storage duration
    - stack objects
      - destroyed at scope end
  - dynamic storage duration
    - heap objects via new/delete
      - prefer smart pointers
  - static storage duration
    - global/static variables
      - initialization order issues
        - static initialization order fiasco
  - thread storage duration
    - thread_local objects
      - lifetime per thread

- References and pointers
  - lvalue references
    - aliasing semantics
      - cannot be null
  - rvalue references
    - move semantics gateway
      - perfect forwarding gateway
  - pointers
    - pointer arithmetic rules
      - array decay rules
        - nullptr checks

- const correctness
  - const objects
    - const member functions
      - logical constness
        - mutable members (careful)
  - constexpr vs const
    - compile-time constants
      - runtime constants
  - const in pointer types
    - pointer to const
      - const pointer
        - const pointer to const

- Initialization (deep)
  - default initialization
    - value initialization
      - zero initialization
        - aggregate initialization
  - brace initialization
    - prevents narrowing
      - initializer_list preference pitfalls
  - copy initialization vs direct initialization
    - implicit conversions difference
      - explicit constructors effect
  - initialization order in classes
    - member order is declaration order
      - base class init order before members

- RAII (resource management)
  - deterministic cleanup via destructors
    - file handles
      - sockets
        - mutex locks
          - memory ownership
  - rule of 0
    - prefer types with correct defaults
      - compose RAII members
  - rule of 5
    - when you manage resources manually
      - copy ctor
      - copy assignment
      - move ctor
      - move assignment
      - destructor

- Copy vs move semantics
  - copy operations
    - deep copy vs shallow copy
      - value types vs owning pointers
  - move operations
    - moved-from valid but unspecified
      - ensure invariants preserved
  - std::move
    - casts to rvalue
      - does not move by itself
  - copy elision
    - NRVO
      - guaranteed elision cases (modern)

- Dynamic memory management
  - new/delete
    - new[]/delete[] mismatch hazards
      - avoid raw new/delete in modern code
  - smart pointers
    - std::unique_ptr
      - single ownership
        - custom deleters
          - pimpl idiom
    - std::shared_ptr
      - shared ownership
        - control block overhead
          - cycles (use weak_ptr)
    - std::weak_ptr
      - break cycles
        - observe without owning
  - allocators (advanced)
    - custom allocator models
      - pmr polymorphic allocators
        - memory_resource

- Undefined behavior awareness (must)
  - use-after-free
    - double delete
      - invalid iterator usage
        - out-of-bounds access
          - signed integer overflow
  - data races are UB
    - even if “seems to work”
      - must synchronize

=====================================================================
FUNCTIONS: SIGNATURES + OVERLOADS + DEFAULTS + LAMBDAS
=====================================================================

- Function declarations
  - prototypes
    - definitions
      - inline linkage behavior
  - parameter passing
    - by value
      - copy cost
        - move optimization opportunities
    - by reference
      - mutating parameters
        - const reference for read-only
    - by pointer
      - nullable optional parameters
        - ownership clarity required

- Overloading
  - overload resolution rules
    - exact match vs promotion vs conversion
      - ambiguity errors
  - const overloads
    - member function constness
      - ref-qualified overloads (& and &&)
  - default arguments
    - set in declarations
      - visible at call site
        - ODR hazards with inconsistent defaults

- Return types
  - by value
    - RVO and move
      - preferred for value types
  - by reference
    - return references only to valid objects
      - no dangling references
  - auto return type
    - trailing return type
      - decltype(auto) nuances

- Lambdas
  - capture modes
    - by value
      - by reference
        - init-capture
          - move capture patterns
  - generic lambdas
    - auto parameters
      - concepts constraints (modern)
  - mutable lambdas
    - allow modifying captured-by-value
  - lambda to std::function
    - type erasure overhead
      - prefer templates where possible

=====================================================================
USER-DEFINED TYPES: STRUCTS, CLASSES, ENUMS, OPERATORS
=====================================================================

- Struct vs class
  - default public vs private
    - same capabilities otherwise

- Class design basics
  - constructors
    - default constructor
      - explicit constructors
        - converting constructors
    - delegating constructors
      - member initializer lists
        - base initialization
  - destructor
    - virtual destructor rules
      - when deleting via base pointer
  - methods
    - const member functions
      - static member functions
        - friend functions

- Encapsulation and invariants
  - private data
    - public API design
      - getters/setters vs behavior methods
        - keep class invariant always valid

- Operator overloading
  - arithmetic operators
    - symmetric vs member vs non-member
      - keep semantics intuitive
  - comparison operators
    - == and <=> patterns
      - define consistent ordering
  - stream operators
    - operator<< for output
      - formatting and locale considerations

- Enums
  - unscoped enum
    - implicit conversions
      - name pollution
  - scoped enum class
    - strong typing
      - explicit underlying types

- Inheritance and polymorphism
  - is-a modeling only
    - prefer composition for has-a
  - virtual functions
    - dynamic dispatch
      - vtable concept
    - override and final
      - correctness and intent
  - abstract base classes
    - pure virtual
      - interface design
  - multiple inheritance
    - diamond problem
      - virtual inheritance
        - complexity and caution

- RTTI and dynamic_cast
  - safe downcasting in polymorphic hierarchies
    - cost and design tradeoffs
  - typeid
    - type identification patterns

=====================================================================
TEMPLATES + GENERICS + METAPROGRAMMING (MODERN STYLE)
=====================================================================

- Function templates
  - type deduction rules
    - reference collapsing
      - forwarding references
  - specialization vs overload
    - partial ordering rules
  - constraints (concepts)
    - requires clause
      - named concepts
        - improves errors and readability

- Class templates
  - template parameters
    - non-type template parameters
      - template template parameters
  - partial specialization
    - pattern matching on types
      - careful design

- Parameter packs
  - variadic templates
    - fold expressions
      - pack expansion patterns

- SFINAE (legacy but common)
  - enable_if
    - detection idiom
      - tag dispatching

- constexpr and compile-time programming
  - constexpr functions
    - constexpr variables
      - consteval
        - immediate functions
  - constexpr containers and algorithms (modern)
    - compile-time evaluation goals
      - reduce runtime overhead

- Type traits
  - std::is_same, is_integral, is_trivial, etc
    - remove_reference, decay, conditional
      - invoke_result, common_type
  - writing generic code safely
    - constrain assumptions explicitly

=====================================================================
THE STANDARD LIBRARY (STL): CONTAINERS, ALGORITHMS, ITERATORS, RANGES
=====================================================================

- Core STL mental model
  - containers store data
    - iterators provide access
      - algorithms operate on iterator ranges
        - function objects customize behavior

- Containers: sequence
  - std::vector
    - capacity vs size
      - reallocation invalidates references/iterators
        - reserve vs resize
  - std::deque
    - stable references? (limited)
      - push/pop at ends
  - std::list / std::forward_list
    - node-based
      - iterator stability
        - cache locality tradeoffs
  - std::array
    - fixed-size
      - stack allocation patterns
  - std::string
    - small string optimization considerations
      - encoding assumptions (UTF-8 handling is not automatic)

- Containers: associative
  - std::map / std::set
    - ordered tree-based
      - comparator requirements
        - logarithmic operations
  - std::unordered_map / std::unordered_set
    - hash-based
      - custom hash + equality
        - rehashing effects

- Containers: adapters
  - std::stack
    - underlying container choice
  - std::queue
    - FIFO adapter
  - std::priority_queue
    - heap adapter

- Iterators
  - iterator categories
    - input/output
      - forward/bidirectional/random-access/contiguous
  - invalidation rules
    - container-specific
      - most common source of bugs

- Algorithms
  - non-modifying
    - find, count, any_of, all_of
  - modifying
    - transform, remove/remove_if, unique
      - erase-remove idiom
  - sorting and ordering
    - sort, stable_sort, partial_sort
      - nth_element
  - numeric algorithms
    - accumulate, inner_product
  - heap algorithms
    - make_heap, push_heap, pop_heap
  - set algorithms (on sorted ranges)
    - set_union, set_intersection

- Function objects and callables
  - std::function (type erasure)
    - overhead vs flexibility
  - std::bind (legacy)
    - prefer lambdas
  - std::invoke
    - unified callable invocation
  - std::reference_wrapper
    - store references in containers

- Ranges (modern)
  - ranges algorithms
    - views pipeline
      - lazy evaluation
        - composability
  - common views
    - filter, transform, take, drop, join
      - iota, reverse
  - borrowing/lifetime considerations
    - dangling view hazards
      - use owning views when necessary

- Utility library
  - std::pair / std::tuple
    - structured bindings
      - tuple utilities
  - std::optional
    - absence of value without nullptr
  - std::variant
    - type-safe union
      - visitation patterns
  - std::any
    - dynamic type container
      - runtime checks
  - std::span
    - non-owning view over contiguous memory
      - safer than raw pointer+size pairs

- Error handling library
  - exceptions
    - std::exception hierarchy
      - throw/catch best practices
  - error codes
    - std::error_code
      - std::system_error
  - assertions
    - assert
      - contract-like defensive checks

=====================================================================
I/O, FILESYSTEM, FORMATTING, TEXT, TIME
=====================================================================

- Streams I/O
  - iostream basics
    - cin/cout/cerr
      - syncing with stdio
        - performance toggles
  - file streams
    - ifstream/ofstream/fstream
      - RAII file handling
        - binary mode concerns
  - string streams
    - istringstream/ostringstream
      - parsing and formatting

- Formatting (modern)
  - std::format style formatting
    - format specifiers
      - type-safe formatting goals

- Filesystem (modern)
  - std::filesystem::path
    - canonical/absolute/relative
      - directory iteration
        - file status queries
  - robust file operations
    - error_code overloads vs exceptions

- Strings and text
  - UTF-8 reality
    - std::string holds bytes, not “characters”
      - grapheme clusters not handled
  - regex (use carefully)
    - performance pitfalls
      - prefer simpler parsing when possible

- Time utilities
  - std::chrono
    - duration types
      - clocks
        - time points
  - measuring performance
    - steady_clock for benchmarks
      - system_clock for wall time

=====================================================================
CONCURRENCY: THREADS, ATOMICS, LOCKS, ASYNC
=====================================================================

- Threading basics
  - std::thread
    - joining vs detaching
      - lifetime hazards
  - mutexes
    - std::mutex
      - std::recursive_mutex (avoid if possible)
    - lock helpers
      - std::lock_guard
        - std::unique_lock
          - std::scoped_lock
  - condition variables
    - std::condition_variable
      - predicate usage pattern
        - spurious wakeups handling

- Futures and async
  - std::async
    - launch policies
      - deferred vs async
  - std::future / std::promise
    - one-shot communication
      - exception propagation
  - packaged_task
    - task wrapper for thread pools

- Atomics and memory model (advanced but critical)
  - std::atomic
    - lock-free vs not lock-free
  - memory ordering
    - relaxed
      - acquire/release
        - seq_cst
  - data races are UB
    - you must synchronize shared mutable state

=====================================================================
DEBUGGING, TESTING, TOOLING, SANITIZERS, PROFILING
=====================================================================

- Compiler warnings and diagnostics discipline
  - enable many warnings
    - fix warnings as bugs
      - use static analysis tools

- Debuggers
  - gdb/lldb basics
    - breakpoints
      - watchpoints
        - backtraces
  - debugging templates
    - inspect instantiated types
      - reduce template complexity when needed

- Sanitizers (find real bugs fast)
  - AddressSanitizer
    - heap/stack/global OOB
      - use-after-free
        - leaks (often via LeakSanitizer)
  - UndefinedBehaviorSanitizer
    - catch UB patterns early
  - ThreadSanitizer
    - detect data races

- Static analysis
  - clang-tidy
    - modernize checks
      - performance checks
        - bugprone checks
  - clang static analyzer
    - path-sensitive analysis
      - null dereference and ownership-like issues

- Testing
  - unit testing frameworks
    - Catch2 / GoogleTest style
      - fixtures
        - parametrized tests
  - property-based testing (advanced)
    - random input generation
      - invariants based tests
  - continuous integration basics
    - build matrix: compilers + standards + OS
      - sanitizers in CI

- Profiling and performance analysis
  - CPU profiling
    - sampling profilers
      - flamegraphs
  - memory profiling
    - allocation hot paths
      - fragmentation observations
  - microbenchmarking
    - avoid measuring noise
      - warmup and stable clocks

=====================================================================
DESIGN: MODERN C++ STYLE, GUIDELINES, ARCHITECTURE
=====================================================================

- Modern C++ coding principles
  - write in ISO standard C++ style
    - express intent
      - keep code statically type-safe where possible
  - prefer RAII and deterministic cleanup
    - no raw owning pointers
      - ownership explicit
  - prefer immutability when possible
    - reduce shared mutable state
      - simplifies concurrency
  - prefer compile-time checking
    - concepts and constexpr
      - reduce runtime failures

- API design
  - value semantics where possible
    - stable invariants
      - minimal surprises
  - error handling strategy
    - exceptions vs error_code vs expected-like patterns
      - consistency across project
  - const-correctness discipline
    - references vs pointers choices
      - span/optional usage patterns

- Common architecture patterns
  - pimpl for ABI stability
    - reduce header dependencies
      - improve compile times
  - dependency injection (lightweight)
    - testability
      - separation of concerns
  - compile-time vs runtime polymorphism tradeoffs
    - virtual dispatch vs templates
      - code size vs performance vs flexibility

=====================================================================
ADVANCED/OPTIONAL: MODULES, COROUTINES, REFLECTION-ADJACENT, ABI
=====================================================================

- Modules (modern)
  - why modules exist
    - replace textual includes
      - reduce compile times
        - improve isolation
  - module interface vs implementation units
    - export boundaries
      - build system support maturity

- Coroutines (modern)
  - coroutine keywords
    - co_await, co_yield, co_return
      - promise type mechanics
  - generators and async tasks
    - custom awaiters
      - composing coroutine pipelines

- ABI and binary compatibility (systems focus)
  - name mangling
    - compiler/stdlib ABI mismatches
      - avoid mixing toolchains incorrectly
  - inline functions and headers
    - ABI changes via headers
      - versioning strategies

=====================================================================
SPECIALIZATION TRACKS (PICK AFTER CORE)
=====================================================================

- Competitive programming C++
  - fast I/O
    - ios::sync_with_stdio(false)
      - cin.tie(nullptr)
  - algorithmic STL mastery
    - vector + sort + binary_search
      - maps/unordered maps pitfalls
        - custom hash for adversarial cases
  - bit tricks and integer math
    - modulo arithmetic
      - overflow-safe patterns
  - debugging speed
    - asserts + small tests
      - sanitizer locally when possible

- Systems/OS C++
  - memory alignment and allocators
    - lock-free structures (advanced)
      - atomics-heavy design
  - networking
    - async I/O libraries
      - protocol parsing and binary formats

- Game/real-time C++
  - cache locality
    - data-oriented design
      - ECS patterns
  - deterministic performance
    - avoid allocations in hot loops
      - custom allocators/pools

- High-performance computing
  - vectorization awareness
    - parallel algorithms (where available)
      - threading models
  - profiling-driven optimization
    - avoid premature optimization
      - validate with benchmarks

=====================================================================
REFERENCE “WHAT EXISTS” MAP (WHERE TO LOOK UP DETAILS)
=====================================================================

- Core language constructs reference
  - declarations, initialization, expressions, statements, classes, templates
    - use a single canonical reference when in doubt
      - verify the exact rules and edge cases

- Standard library reference
  - containers, iterators, algorithms, concurrency, filesystem, utilities
    - learn by categories
      - then by header-level organization

- Best-practice guidelines
  - modern style, resource safety, type safety, performance guidance
    - apply as a quality layer after learning basics

- Build system reference
  - target-based modeling, transitive deps, presets, generators
    - essential for real projects
      - learn enough to structure multi-file repos
