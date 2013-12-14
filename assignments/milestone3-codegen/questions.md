# Milestone

#### My menu entries keep dissapearing

This is due to a bug in one of the dependencies of spoofax, which sometimes trows a NullPointerException.
There is no known solution at the time, but for some people upgrading from Eclipse 4.2 to 4.3 decreased the problem occurances.
As a workaround, you can restart eclipse with File->Restart. Eclipse should restore all windows etc. and your menu should be complete again.

#### Why is the VarRef constructor defined in such a funky way?

This question might not belong in this milestone but it has been bothering me for some time now.

	VarRef      : ID -> VarRef
				: VarRef -> Exp

Is the above definition equal to the following?

	VarRef : ID -> Exp