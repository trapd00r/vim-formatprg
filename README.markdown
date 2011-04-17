# vim-formatprg

This is a collection of scripts that takes input from vim, transforms it, and
returns it. Contributions very welcome.

# EXAMPLES

You have the following text in pod:

    =head1 A HEADER

    =head2 A smaller header

    Some description, along with some L<links> to L</useful|stuff>.

    Perhaps C<some code>, a little B<bold> and a pinch of C<italics>.

    =cut

Issue this in vim:

    :set formatprg=bin/pod2markdown

Use visual block mode and select the lines you want to transform;

    <C-v>10jj

Followed by the magic **gq** command:

    gq

The text will be turned into:

    # A HEADER

    ## A smaller header

    Some description, along with some [links](http://search.cpan.org/perldoc?links) to [/useful](http://search.cpan.org/perldoc?stuff).

    Perhaps `some code`, a little __bold__ and a pinch of `italics`.
