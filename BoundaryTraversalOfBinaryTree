//GFG Practice

class Solution
{
	ArrayList <Integer> boundary(Node node)
	{
	    ArrayList<Integer> ans = new ArrayList<Integer>();
        if(node.left == null  && node.right == null){
            ans.add(node.data);
            return ans;
        }
        ans.add(node.data);
        addLeftNodes(node.left , ans);
        addLeafNodes(node , ans);
        addRightNodes(node.right , ans);
        return ans;
    }
    
    void addLeftNodes(Node node , ArrayList<Integer> ans){
        if(node == null)    return;
        
        if(node.left != null){
            ans.add(node.data);
            addLeftNodes(node.left , ans);
        }
        else if(node.right != null){
            ans.add(node.data);
            addLeftNodes(node.right , ans);
        }
        return ;
    }
    
    void addLeafNodes(Node node , ArrayList<Integer> ans){
        if(node == null)    return;
        addLeafNodes(node.left , ans);
        addLeafNodes(node.right , ans);
        
        if(node.left ==null && node.right == null){
            ans.add(node.data);
        }
        return;
    }
    
    void addRightNodes(Node node , ArrayList<Integer> ans){
        if(node == null)    return;
        
        if(node.right != null){
            addRightNodes(node.right , ans);
            ans.add(node.data);
        }
        else if(node.left != null){
            addRightNodes(node.left , ans);
            ans.add(node.data);
        }
	}
}
