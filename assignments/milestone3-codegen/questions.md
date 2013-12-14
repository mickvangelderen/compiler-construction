# Milestone

#### My menu entries keep dissapearing

This is due to a bug in one of the dependencies of spoofax, which sometimes trows a NullPointerException.
There is no known solution at the time, but for some people upgrading from Eclipse 4.2 to 4.3 decreased the problem occurances.
As a workaround, you can restart eclipse with File->Restart. Eclipse should restore all windows etc. and your menu should be complete again.

#### How do I enable the desugar builder in the MiniJava project provided for milestone 3?

I tried adding the following code to trans/minijava.str:

	debug-show-desugared:
	    (selected, position, ast, path, project-path) -> (filename, result)
	    with
	      filename := <guarantee-extension(|"desugared.aterm")> path;
	      result   := selected

The string `debug-show-desugared` can be found in include/MiniJava.packed.esv but all this didn't work.