# Rust Data Structures

| Data Structure                                             | Description                                                |
|------------------------------------------------------------|------------------------------------------------------------|
| [Array ([T; N])](Array.md)                                 | Fixed-size collection of elements of the same type.        |
| [Tuple ((T1, T2, ...))](Tuple.md)                          | Fixed-size collection of elements that can be of different types. |
| [Vector (Vec<T>)](Vector.md)                               | Dynamic-size collection of elements of the same type.      |
| [String (String)](String.md)                               | Dynamic-size collection of characters, used for owned strings. |
| [&str (string slice)](Str.md)                              | Immutable view into a string, either a part of a `String` or a string literal. |
| [HashMap (HashMap<K, V>)](HashMap.md)                      | Key-value store with unique keys.                          |
| [BTreeMap (BTreeMap<K, V>)](BTreeMap.md)                   | Key-value store with keys sorted.                          |
| [HashSet (HashSet<T>)](HashSet.md)                         | Collection of unique values.                               |
| [BTreeSet (BTreeSet<T>)](BTreeSet.md)                      | Collection of unique values sorted.                        |
| [LinkedList (LinkedList<T>)](LinkedList.md)                | Doubly-linked list.                                        |
| [BinaryHeap (BinaryHeap<T>)](BinaryHeap.md)                | Priority queue implemented with a binary heap.             |
| [VecDeque (VecDeque<T>)](VecDeque.md)                      | Double-ended queue.                                        |
| [Rc (Rc<T>)](Rc.md)                                        | Reference-counted smart pointer for single-threaded scenarios. |
| [Arc (Arc<T>)](Arc.md)                                     | Reference-counted smart pointer for multi-threaded scenarios. |
| [RefCell (RefCell<T>)](RefCell.md)                         | Interior mutability type for single-threaded scenarios.    |
| [Mutex (Mutex<T>)](Mutex.md)                               | Interior mutability type for multi-threaded scenarios.     |
| [RwLock (RwLock<T>)](RwLock.md)                            | Reader-writer lock allowing concurrent reads or exclusive write. |
| [Option (Option<T>)](Option.md)                            | Represents an optional value.                              |
| [Result (Result<T, E>)](Result.md)                         | Represents a value that may be an error.                   |
| [Cell (Cell<T>)](Cell.md)                                  | A form of interior mutability where `T` is Copy.           |