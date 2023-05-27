# project-short-tools
passwrod visula show and hide button code 
 
   const [password, setPassword] = useState('');
   const [showPassword, setShowPassword] = useState(false);

   const togglePasswordVisibility = () => {
     setShowPassword(!showPassword);
  };

 <input type={showPassword ? 'text' : 'password'} value={password} onChange={(e) => setPassword(e.target.value)} placeholder="Enter your password" 
 className="input input-bordered"/>
 <button onClick={togglePasswordVisibility}>{showPassword ? 'Hide Password' : 'Show Password'}</button>
