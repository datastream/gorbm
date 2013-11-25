# Example

> Training layer 0: numv+1 visible units -> y hidden units
> visible/hidden units with addtion bias unit, but t.String() will not include bias unit.

    weights := []rbm.Vector{
                rbm.RandomMatrix((numv+1)*(y+1), 0.5),
    }

    // len(training[0]) == numv
    training := []rbm.Vector{
            rbm.Vector{1,1,0,0,1},
            rbm.Vector{0,0,1,1,1},
            rbm.Vector{0,1,1,1,0},
    };
    // numv is number of visible units
    r := rbm.CreateRBM(numv, weights)
