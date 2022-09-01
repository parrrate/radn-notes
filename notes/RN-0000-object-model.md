# Object Model
## References
* Each object can be referenced by its hash
* Each reference can re *resolved* (what "resolved" means depends on the execution context) to the referenced object
* Depending on the execution context, object's hash may use the reference list as an additional input
## Serialization
* Each object can be represented as a finite byte sequence and its factory
* Each object can be reconstructed from a valid finite byte sequence and corresponding factory
