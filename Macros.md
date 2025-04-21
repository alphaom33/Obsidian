#limd
Goals:
	full macros, allowing any possibility
	able to be treated as first-class citizens
	~~compiled ahead of time~~ maybe as an optimization later, but impossible to fully do

Ideas:
	tracing to generate macros based on possible code paths
		macro arguments require types, and are treated as functions somehow


(defmacro [$asdf:delimiter]
	`$asdf 1 2 $asdf`)

possibilities:
	(1 2)
	[1 2]
	{1 2}

gen foreach
cons:
	so many