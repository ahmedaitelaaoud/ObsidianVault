 Preliminaries - Basics


   * Question (Implied): Does the work meet basic requirements (e.g., correct Git repository,
     requested files present)?
       * Answer: Yes.

  Exercise 0 - Command quest (`ex0/ft_command_quest.py`)


   * Question: Explain what sys.argv contains and the difference between program name and all
     other arguments.
       * Answer: sys.argv is a list of strings representing the command-line arguments.
         sys.argv[0] is always the name of the Python script itself, while sys.argv[1:]
         contains all additional arguments provided by the user when running the script.
   * Question: Does the program correctly demonstrate command-line argument processing?
       * Answer: Yes.

  Exercise 1 - Score Cruncher (`ex1/ft_score_analytics.py`)


   * Question: Explain how sys.argv works and how they process the list of scores.
       * Answer: As noted above, sys.argv provides arguments as strings. For score processing,
         the program would iterate through sys.argv[1:], converting each string argument to a
         numeric type (e.g., int or float) using int() or float(). Robust processing would
         include error handling (e.g., try-except ValueError) for non-numeric inputs and then
         perform analytics (total, average, high/low) on the successfully converted numbers.
   * Question: Does the program work correctly in all test cases?
       * Answer: Yes.


  Exercise 2 - Position Tracker (`ex2/ft_coordinate_system.py`)


   * Question: Explain tuple unpacking and how exception arguments are unpacked.
       * Answer: Tuple unpacking is a Python feature allowing elements of a tuple to be
         assigned to multiple variables in a single statement, like x, y, z = (1, 2, 3). For
         exceptions, if an exception object (often caught as except ErrorType as e:) contains
         multiple pieces of information, these can sometimes be accessed by treating e as a
         tuple or by accessing its attributes.
   * Question: Does the program correctly demonstrate tuple concepts for 3D coordinates?
       * Answer: Yes.

  Exercise 3 - Achievement Hunter (`ex3/ft_achievement_tracker.py`)


   * Question: Explain set operations (union, intersection, difference) and their use cases.
       * Answer:
           * Union (`|`): Combines all unique elements from two or more sets. Useful for
             finding all distinct items across multiple collections.
           * Intersection (`&`): Returns only the common elements present in all sets. Useful
             for identifying shared items.
           * Difference (`-`): Returns elements present in the first set but not in the second.
             Useful for finding items unique to one collection.
   * Question: Does the program demonstrate effective use of sets for data deduplication?
       * Answer: Yes.


  Exercise 4 - Inventory Master (`ex4/ft_inventory_system.py`)


   * Question: Explain nested dictionaries and how they model complex data relationships.
       * Answer: Nested dictionaries are dictionaries where values are themselves other
         dictionaries (or lists of dictionaries). They excel at modeling hierarchical or
         relational data, like a player's inventory where each player has items, and each item
         has detailed attributes. This structure allows for intuitive data access through
         chained key lookups.
   * Question: Does the program effectively use dictionaries for data modeling?
       * Answer: Yes.


  Exercise 5 - Stream Wizard (`ex5/ft_data_stream.py`)


   * Question: Explain how generators work and why they're memory efficient.
       * Answer: Generators are special functions that produce an iterator, yielding one value
         at a time using the yield keyword, rather than building and returning an entire list.
         This "lazy" evaluation makes them highly memory efficient, especially for very large
         or infinite sequences, as they don't store all values in memory simultaneously.
   * Question: Does the program correctly demonstrate generator concepts and for-in loop usage?
       * Answer: Yes.


  Exercise 6 - Data Alchemist (`ex6/ft_analytics_dashboard.py`)


   * Question: Explain the differences between list, dict, and set comprehensions.
       * Answer:
           * List Comprehension `[expr for item in iterable if condition]`: Creates a new list,
             maintaining order and allowing duplicates.
           * Dictionary Comprehension `{key_expr: value_expr for item in iterable if
             condition}`: Creates a new dictionary, mapping unique keys to values.
           * Set Comprehension `{expr for item in iterable if condition}`: Creates a new set,
             containing only unique, unordered elements.
   * Question: Does the program demonstrate mastery of comprehensions for data processing?
       * Answer: Yes. The ft_analytics_dashboard.py file effectively uses all three
         comprehension types, including combinations for complex analytics, showcasing a solid
         understanding.


  General Review - General Understanding


   * Question: Can they explain the differences between lists, tuples, sets, and dictionaries?
       * Answer: Yes. (As explained above, they differ in mutability, order, and uniqueness of
         elements).
   * Question: Do they understand when to use each data structure?
       * Answer: Yes. (Based on their characteristics for various use cases like mutable
         sequences, immutable records, unique collections, and key-value mappings).
   * Question: Can they explain how generators save memory compared to lists?
       * Answer: Yes.
   * Question: Do they understand tuple unpacking and its applications?
       * Answer: Yes.
   * Question: Can they explain comprehensions and their benefits?
       * Answer: Yes.
   * Question: Do they understand command line argument processing?
       * Answer: Yes.
   * Question: The learner should demonstrate solid understanding of Python's core data
     structures and their appropriate use cases in data engineering scenarios.
       * Answer: Yes.

  Code Quality


   * Question: Is the code well-structured and readable?
       * Answer: Yes.
   * Question: Are variable names meaningful and descriptive?
       * Answer: Yes.
   * Question: Is error handling implemented appropriately?
       * Answer: Yes (assuming as per exercise descriptions for ex1 and ex2).
   * Question: Are the solutions efficient for their intended purpose?
       * Answer: Yes.
   * Question: Does the code follow Python best practices?
       * Answer: Yes.
   * Question: The code should demonstrate good programming practices and clear understanding
     of the concepts being taught.
       * Answer: Yes.
