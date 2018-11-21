전체적으로 BST_TREE와 비슷하지만 AVL_TREE는 left와 right의 높이 차이가 2 이상이 되지않는 tree 이다.  
양 쪽의 높이를 유지해주기 위하여 노드를 삽입할 때마다 rotate를 이용해서 balance를 맞춘다.  
  
T_NODE* rotate_left(T_NODE* root){  
-루트의 오른쪽부터 왼쪽으로 회전시켜주면서 right가 새로운 루트가 된다.  
  
T_NODE* rotate_right(T_NODE* root){  
-루트의 왼쪽부터 오른쪽으로 회전시켜주면서 left가 새로운 루트가 된다.  
  
T_NODE* insert_rotate(T_NODE* root,T_NODE* new_node,bool* taller){  
-현재 루트가 왼쪽의 높이가 높은지,오른쪽이 높은지,높이가 같은지를 이용해서 밸런스를 맞추어준다.  
-이를 위해 node에 balance값이 필요하고 balance를 맞추는 함수가 필요하다.  
  
T_NODE* balance_left(T_NODE* root,bool* taller){  
-노드가 삽입된 상태에서 왼쪽,오른쪽의 높이를 구한다.  
-높이를 맞추기 위하여 회전이 되기 전에 회전이 된 후에 변하게될 값들을 미리 바꾸어 놓는다.  
-높이에 맞게 회전시킨다.  
