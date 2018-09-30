# LCA
My name is Aoife and I am studying computer engineering. This is a college assignment where we will implement a structure that can calculate the lowest common ancestor in a graph that may be constructed as a binary tree. 


import lowestCommonAncestor.node
public class lowestCommonAncestor {
	  // Source:
		// http://www.fusu.us/2013/06/p2-lowest-common-ancestor-in-binary-tree.html
		// Adapted
    
public static Node lowestCommonAncestor(Node root, Node a, Node b){
if( root == null){
return null;
}
if (root.equals(a) || root.equals(b)) {
return root 
}
// if one is matched there is no need to continue as this is the LCA
Node l = lowestCommonAncestor(root.getSuccesor1(), a, b);
Node r = lowestCommonAncestor(root.getSuccesor2(), a, b);
if(l!=null && r !=null){
return root;
}
//this will show that the nodes are on seperate branches
return l!= null ? l:r;
}
}
}
