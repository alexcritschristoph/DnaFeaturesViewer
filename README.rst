This is my modified repository of the 'Dna Features Viewer' from Edinburgh Genome Foundry. This is a nice little library, but I decided to modify it for a specialized use case - visualizing operons of genes on contigs.


License
---------

Dna Features Viewer is an open-source software originally written at the `Edinburgh Genome Foundry
<http://edinburgh-genome-foundry.github.io/home.html>`_ by `Zulko <https://github.com/Zulko>`_
and `released on Github <https://github.com/Edinburgh-Genome-Foundry/DnaFeaturesViewer>`_ under the MIT licence.
Everyone is welcome to contribute !

Installation
--------------

.. code:: python

    sudo python setup.py install



Examples of use
----------------


Basic plots
~~~~~~~~~~~~

In this first example we define features "by hand":

.. code:: python

    from dna_features_viewer import GraphicFeature, GraphicRecord
    features=[
        GraphicFeature(start=0, end=20, strand=+1, color="#ffd700",
                       label="Small feature"),
        GraphicFeature(start=20, end=500, strand=+1, color="#ffcccc",
                       label="Gene 1 with a very long name"),
        GraphicFeature(start=400, end=700, strand=-1, color="#cffccc",
                       label="Gene 2"),
        GraphicFeature(start=600, end=900, strand=+1, color="#ccccff",
                       label="Gene 3")
    ]
    record = GraphicRecord(sequence_length=1000, features=features)
    record.plot(figure_width=5)

.. figure:: https://raw.githubusercontent.com/Edinburgh-Genome-Foundry/DnaFeaturesViewer/master/examples/by_hand.png
    :align: center
