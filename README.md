This project is aimed at using ngl view to render pairwise interaction networks onto protein structures directly in
ipython notebooks using packages nglview and pytraj.

For now, a rudimentary function has been created that will iterate over all non-zero entries of a matrix and render
edges connecting corresponding residue alpha carbons. E.g. each entry of the matrix is taken to represent an interaction
between pairs of residues in the protein.

Each edge gets rendered as a cylinder. Cylinder radii (edge thickness) can be controlled by passing a corresponding matrix.
Color can be controlled by passing an MxNx3 array consisting of entries which are numbers in the range 0-1.
E.g. if the edge from residue 0 to residue 1 should be red, then set colorArray[0,1,:]=[1.0,0.0,0.0].
