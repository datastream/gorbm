# Example

> Training layer 0: (numv+1) visible units -> x hidden units

    weights := []rbm.Vector{
                rbm.RandomMatrix((numv+1)*x, 0.5),
    }

    // len(training[0]) == numv
    training := []rbm.Vector{
            rbm.Vector{1,1,0,0,1},
            rbm.Vector{0,0,1,1,1},
            rbm.Vector{0,1,1,1,0},
    };
    // numv is number of visible units
    r := rbm.CreateRBM(numv, weights)
