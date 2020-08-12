# Alpha-beta-pruning-search-
## Perform Alpha-beta pruning search on random100 number.The brut force method will be accepted.Neat Documentation is expected with from scratch implementation with c++
Alpha-Beta pruning is not actually a new algorithm, rather an optimization technique for minimax algorithm. It reduces the computation time by a huge factor. This allows us to search much faster and even go into deeper levels in the game tree. It cuts off branches in the game tree which need not be searched because there already exists a better move available. It is called Alpha-Beta pruning because it passes 2 extra parameters in the minimax function, namely alpha and beta.

The ideal ordering for alpha-beta pruning occurs when lots of pruning happens in the tree, and best moves occur at the left side of the tree. We apply DFS hence it first search left of the tree and go deep twice as minimax algorithm in the same amount of time
## Algorithm:
function alphabeta(node, depth, α, β, Player) 

• if depth = 0 or node is a terminal node 

• return the heuristic value of node 

• if Player = MaxPlayer

• for each child of node 

• α := max(α, alphabeta(child, depth-1, α, β, not(Player) )) 

• if β ≤ α

• break ; Prune

• return α

• else

• for each child of node 

• β := min(β, alphabeta(child, depth-1, α, β, not(Player) ))

• if β ≤ α break ; Prune

• return β

• end

• Initial call

• alphabeta(origin, depth, -infinity, +infinity, MaxPlayer)
