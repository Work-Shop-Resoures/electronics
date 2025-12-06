# history
- was originally designed to allow (embryonic) UNIX operating system
to be easily ported to architectures beyond PDP-11

- was eventually implemented on many platforms, from tiny 8-bit MCUs to
64-bit supercomputers

- when standardised in 1989, aimed to include as much existing code
as possible, so imposed minimal restrictions

-- `char` is the basic unit of memory allocation,
at least 8 bits, but may be larger (e.g. Cray X-MP: 64 bits)

-- `int` is (intended to be) the CPU's native integer type,
at least 16 bits, but may be larger (e.g. Cray X-MP: 64 bits)

# data types
## builtin

- `char` for characters
(guaranteed range 0..127)

- `signed char`, `unsigned char` for very small integers
(guaranteed range (8-bit) -127..127, 0..255)

- `short`/`signed short`, `unsigned short` for small integers
(guaranteed range (16-bit) -32767..32767, 0..65535,
but at least as big as `char`)

-`int`/`signed int`, `unsigned int` for integers
(guaranteed at least as big as `short`)

- `long`/`signed long`, `unsigned long` for large integers
(guaranteed range (32 bit) -2e9..2e9, 0..4e9,
but at least as big as `int`)

- `long long`/`signed long long`, `unsigned long long` for really large integers
(guaranteed range (64 bit) -9e18..9e18, 0..18e18,
but at least as big as `long`)

-- `float` is a floating-point type with at least 6 decimal digits of precision,
guaranteed range 1e-37..1e37 

-- `double` is a floating-point type with at least 10 decimal digits of precision,
guaranteed range 1e-37..1e37

-- `long double` is a floating-point type with at least 10 decimal digits of precision,
guaranteed range 1e-37..1e37

## aggregates

### array

- used when you have a bunch of identical things that will be treated interchangably

- elements can be any existing type (including e.g. another array)

- every element occupies the same amount of space

- define with `{base-type} array_name[number_of_elements];`

- access each element with `array_name[element_number]`
(first element is 0, last element is `number_of_elements-1`)

### structure

- used when you have a group of things that "belong" together 

- fields (elements) can be any combination of existing types
(including e.g. another structure)

- each field has its own name

- define with
```struct struct_tag_name {
	{some-type-1} field_name_1;
...
	{some-type-n} field_name_n;
} structure_name;```

- access field with `structure_name.field_name_x`


# declaration versus definition

- a *declaration* is an announcement that "the name `name` exists,
and has these properties, but details are elsewhere"

-- e.g.
```extern int x;//no space reserved for x yet
struct tagname;//we don't even know how big this structure is
int funcname(float farg, char carg);//function funcname takes farg and carg, returns int```

- a *definition* is the details

