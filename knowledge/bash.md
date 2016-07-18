# The Set Builtin
set -e

exit immediately if a pipline returns a non-zero status


# if else


If [ conditional expression ]
then
	statement1
	statement2
	.
else
	statement3
	statement4
	.
fi


# positional arguments
Executing

`./script.sh Hello World`
Will make

<code>
$0 = script.sh
$1 = Hello
$2 = World
</code>


($#) Expands to the number of positional parameters

# function
function_name () 
{

}
